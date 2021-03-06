# Instructions
1. Read about the Gson project below. 
2. Go to the [Issues tab](https://github.com/invariants-studies/gson0/issues) and click on Issue #1.
3. Read about the issue and begin the tasks described to address the issue. 
4. Once you're finished, submit a PR to close the issue.
5. Let us know once you've submitted the PR.
6. Refer to the issue number for the order in which you should complete them.

# Gson
The [Gson open source project](https://github.com/google/gson) is a Java library that can be used to convert Java objects to their [JSON representation](https://github.com/invariants-studies/gson0#json). It can also be used to convert a JSON string to an equivalent Java object. Gson can work with arbitrary Java objects including pre-existing objects that you don't have the source code for.

There are a few open source projects that can convert Java objects to JSON. Most of these open source projects require that you add Java annotations to your classes. However, you can't add these annotations if you don't have access to the source code. Also, most of these open source projects don't fully support the use of Java Generics. Gson considers each of these to be very important design goals.

# Gson Example
The following code example from the [Gson User Guide](https://github.com/google/gson/blob/master/UserGuide.md#object-examples) shows the serialization and deserialization of a Gson object:
```
class BagOfPrimitives {
  private int value1 = 1;
  private String value2 = "abc";
  BagOfPrimitives() {
    // no-args constructor
  }
}

// Serialization
BagOfPrimitives obj = new BagOfPrimitives();
Gson gson = new Gson();
String json = gson.toJson(obj); 
// ==> String json is {"value1":1,"value2":"abc"}

// Deserialization
BagOfPrimitives obj2 = gson.fromJson(json, BagOfPrimitives.class); 
// ==> BagOfPrimitives obj2 is just like obj
```

# JSON
[JavaScript Object Notation (JSON)](https://www.json.org/json-en.html) is a plain text format for storing and transporting data. Since the format is text only, JSON data can easily be sent between computers and used by any programming language.

# JSON Example
This example is a JSON string:
```
{"name":"Artoo", "class":"Astromech", "equipment":"Saw"}
```

It defines an object with 3 properties:
- name
- class
- equipment

Each property has a value. If you parse the JSON string with a JavaScript program, you can access the data as an object:
```
let droidName = obj.name;
let droidClass = obj.class;
let driodEquipment = obj.equipment
```
