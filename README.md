# lazymongo  

**lazymongo** an Apache 2.0-licensed mongodb orm framework.  
By contributing code to this repository, you agree to make your contribution available under an Apache 2.0 license.  
**lazymongo**  support all the primary data types like boolean, int, long, float, double and String.  
It also support collections and map, the combination of these primary types , collections, map, including embedded document are supported as well.  
The official mongodb driver don't support such complex combinations.  
Flexibility is the goal of this library, it fit for small datasets, if you are going to pull out a huge amount of documents into a List, then OOM may occurs. 

**lazymongo** would utilize the power of compiler to perform static analysis of your query to avoid the spelling mistake of table name or field name.  

usage:  
insert document  
BasicPoJo pojo = new BasicPoJo();  
pojo.insert();  

update document  
BasicPoJo pojo = new BasicPoJo();  
pojo.setName("newName");  
pojo.update();

find one document  
BasicPoJo pojo =BasicPoJo.findFirst(BasicPoJo.class, eq("id", idvalue));  

find list of document  
List\<BasicPoJo\> pojos =BasicPoJo.findAny(BasicPoJo.class, eq("id", idvalue));  

delete one document  
BasicPoJo pojo =BasicPoJo.findFirst(BasicPoJo.class, eq("id", idvalue));  
pojo.delete();

count number of documents    
int number =BasicPoJo.count(BasicPoJo.class, eq("id", idvalue));    

aggregate support would be added later  

enjoy **lazymongo** and save your life ;)  








