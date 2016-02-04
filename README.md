1. Carteasy

A Shopping cart library for Android that allows you add to add items to cart and retrieve at ease.

2. Quick Start

Add the following dependency to your build.gradle:

//Dependecies will come here.

You should then checkout the library and investigate the sample code, which covers some of the features.

<image of sample app here>

3. Usage

 *Adding items to cart*

 ```
 Carteasy cs = new Carteasy();
 cs.add(String id, String key, Object value);
 cs.commit(getApplicationContext());
 ```

 ```
 cs.add("Your Product Id", "key", "value");
 ```


 Your product items is tied to your Id and can be retrieved anytime the Id is produced.

 ```
 String productIdOne = "e400";
 String productIdTwo= "e401";
 ```

 ```
 Carteasy cs = new Carteasy();

 cs.add(productIdOne, "product name", "Marlboro");
 cs.add(productIdOne, "product description", "cigarate box");
 cs.add(productIdOne, "product price", 200.00);
 cs.add(productIdOne, "quantity", 5);
 cs.add(productIdOne, "currency", "dollar");
 ...

 cs.add(productIdTwo, "product name", "Starbucks coffee");
 cs.add(productIdTwo, "product description", "coffee bags");
 cs.add(productIdTwo, "product price", 100.00);
 cs.add(productIdTwo, "quantity", 9);
 cs.add(productIdTwo, "currency", "dollar");
 ...
 cs.commit(getApplicationContext());
 ```


 *Retrieve item by Id and key*

 Returns an object. you can use it as an object or typecast it to what ever you want

 ```
 Carteasy cs = new Carteasy();
 Object value = cs.get( String id, String key, getApplicationContext());
 ```

 Returns a String

 ```
 Carteasy cs = new Carteasy();
 String value = cs.getString( String id, String key, getApplicationContext());
 ```

 You can return type of value using either of these below:

 *String*

 ```
 cs.getString(String id, String key, Context context);
 ```

 *Integer*

 ```
 cs.getInteger(String id, String key, Context context);
 ```

 *Float*

 ```
 cs.getFloat(String id, String key, Context context);
 ```

 *Double*

 ```
 cs.getDouble(String id, String key, Context context);
 ```

 *Long*

 ```
 cs.getLong(String id, String key, Context context);
 ```

 *Short*

 ```
 cs.getShort(String id, String key, Context context);
 ```


 *Update Items*

 To update a items value, you have to pass the id, key and your newValue as parameters

 ```
 Carteasy cs = new Carteasy();
 cs.update(String id, String key, Object newValue, Context context);
 ```

 *Removing specific item value from cart*

 ```
 Carteasy cs = new Carteasy();
 cs.Removekey(String id, String key, Context context);
 ```

 *Removing item and its property value from cart*

 ```
 Carteasy cs = new Carteasy();
 cs.RemoveId(String id, Context context);
 ```



*Caveats*

Nothing here for now.



*Credits*

This library depends on json-simple-1.1.1

