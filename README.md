# Gson
[Gson](https://github.com/google/gson) is a Java library that can be used to convert Java objects into their [JSON](https://github.com/invariants-studies/gson0/blob/master/README.md#json) representation. It can also be used to convert a JSON string to an equivalent Java object. Gson can work with arbitrary Java objects including pre-existing objects that you do not have the source code for.

There are a few open source projects that can convert Java objects to JSON. However, most of them require that you place Java annotations in your classes; something that you can not do if you do not have access to the source code. Also, most of these open source projects do not fully support the use of Java Generics. Gson considers both of these as very important design goals.

# Gson Example
This example shows serialization and deserialization of a Gson object:
```
class BagOfPrimitives {
  private int value1 = 1;
  private String value2 = "abc";
  private transient int value3 = 3;
  BagOfPrimitives() {
    // no-args constructor
  }
}

// Serialization
BagOfPrimitives obj = new BagOfPrimitives();
Gson gson = new Gson();
String json = gson.toJson(obj);  
// ==> json is {"value1":1,"value2":"abc"}

// Deserialization
BagOfPrimitives obj2 = gson.fromJson(json, BagOfPrimitives.class);
// ==> obj2 is just like obj
```

# JSON
JavaScript Object Notation (JSON) is a plain text format for storing and transporting data. Since the format is text only, JSON data can easily be sent between computers and used by any programming language. 

# JSON Example
This example is a JSON string:
```
'{"name":"John", "age":30, "car":null}'
```

It defines an object with 3 properties:
- name
- age
- car

Each property has a value. If you parse the JSON string with a JavaScript program, you can access the data as an object:
```
let personName = obj.name;
let personAge = obj.age;
```
# Web Client–Server Relationships
We can categorize technologies as client side or server side:
- On the client side, we have HTML, CSS, and JavaScript
- On the server side, there is PHP, ASP.NET, Node.js, Ruby on Rails, Java, Go, etc.

As a web client, we send requests for resources to a server using HTTP. The server responds with a document, such as HTML or JSON. When that document is a JSON document, the server side code must handle the creation of it.

In addition to serving a JSON document, a server may receive a JSON document. When a document is received, the server-side code must handle the parsing of that document.

JavaScript can make behind-the-scenes HTTP requests for JSON resources to web APIs. It’s easy to think of JavaScript playing this role because it is categorized as “client side.” However, JavaScript isn’t the only language that can make HTTP requests for JSON resources. HTTP requests can also be made by a server-side web framework. In the scenario where JSON is requested by a server-side technology, its role becomes the client.

