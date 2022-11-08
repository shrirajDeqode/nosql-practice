SQL vs NOSQL -

	SQL -

	it is an Relational database.
	Have well define strucutre or schema, requires querry langauage for operation(SQL).
	SQL follows ACID properties (Atomicity, Consistency, Isolation and Durability) .
	performance is slow in case of complex querry as having joins.
	Vertically scalable (we can incease Computing poewer).

	NoSQL -

	It can have no or minimum relations.
	do not need to think much about well defined schema.Supports unstructured data.
	Follows CAP theorem (Consistency, Availability and Partition tolerance).
	Prformance is fast .
	Horizontally as well as vertically scalable.

	What to choose & when - if we want more static and well defined structure and also if we want to maintain relations between the schema and if it includes lot of       update operation over schema then in that casse choose SQL databases, But if we want freedom from well organised structured data and also we want great performance     & also having large data with minmum update operation and majore read operations then go for NOSQL.


CAPS Theorem - 

	Imp point from distributes system design point of view.Distributes system is nothing but a system that consist of many machines that work in sycn or cordination so     that end user will fill like there is only one machine.

	Consistency - Any read that is happening after a latest write , all the nodes should return the latest value of that write.It refers to data replication.
	
	Availability - Every node in the system should respond in a non error format to any read request without the guarantee of returning the latest write.
	
	Partition tolerance - System will be responding to all read and write even if the communication channel between nodes is borken.Mainly happen due to network           failure.If partition happens then we need to let go eighter consistency or avaialability.
	
	Use case - if we want to apply CAP theorem in some imp domain like financial in that case we need to choose consistency over avaialability otherwise in other case we   can let go consistency over avaialability.
		
