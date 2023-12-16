Variables -
ES 5 
   - var
ES 6 
   - let 
   - const

Definition of var :

Var is Declaration + Assignment , which means that it will declare a value of a container and also assign it. (The system considers the latest declaration of var)

For Example :

var (container) = (value);
var c = 10; (Declaration + Assignment)
var c = 8; 
var c = 9;
var c = 7; (This is considered as the value as it is the latest declaration)

Definiton of let :

Let is also Declaration + Assignment. In let , after a value is declared and assigned , it can later be changed.

For example :

let c = 9; (Declaration + Assignment)

c = 8; (Declaration)

Note - let should only be used once in a file, to change the value - just write the container name and value    

Definition of const :

Once a value is declared , it can not be changed.

For example :

const c = 9;

c = 8; <wont work>

To work on node :

1. Create a file with extension .js
2. Write the command [ console.log('text') ]
3. Open the terminal 
4. Run the command node (file name)
5. It will print the value

For exzmple :

-var/let/const a = 8; (needs to be written before console.value so that value can be defined)
-console.value(8)
-Either go to terminal or to the console of the browser
-Run node <file name>
Result : 8


{
    (anything inside this is lexical)
}

functional c() {
    (anything inside this becomes a functional scope)
}

When written console.log(typeof <container>)
prints the type of the value the container contains

Primitive 
-string
-number
-boolean
-undefined
-null
-symbol

Non-Primitve 
-object
    -{ key(string): 'value'} Like
                - var a = {
                    hello : 'value',
                    hello1 : 10,
                }
    -number
    -string
    -null
    -boolean
    -object
    -array
    -undefined
-array
    -[]

    PRACTICE :

    var a = 10;

    var b;

    b = a 

    [b's value is 10]

    var c;

    c = 11;

    a = c;

    [a's value 11]

How to set dynamically
- hello.location = "Jamshedpur";

Popular Confusion:

var a = 10;
b = a;
b = 20;
console.log("a")
console.log("b")
node file.js
10 20

It is because in this the value is assigned primitve.

Whereas;

var a = {
    string : "hello",
}
var b;
b = a;
b.name = "Hello2"
console.log("a", a)
console.log("b", b)
node file.js
a {string: "hello", name: "Hello2"}
b {string: "hello", name: "Hello2"}

To overwrite b = {};

TO CASTE AS A NUMBER:
container = Number(container);
container = parseInt(container); [Same as number but ignores all the digits after decimal]

When + is added before a value it converts it into a number , if it is not a number it will show NaN

&& reprersents (And) 
It means that if any one of the two values is false , then the total value is false

Whereas 

|| represents (or)
It means that if any one the two values is true , then the total value is true

value1 = "Hello";
value2 = "World";

if(value1 && value2){
}else{

}
 
USE ? AS A SUBSTITUTE

value1 = "";
value2 = "2nd value";

tvalue = value1 && value2;
Console.log(tvalue)

Result - 2nd value (It always assigns the second value)

Ternery should be written as 

var val3 = ( val1 || val2 ) ? 10 : 20;
console.log(val3);

After using let once , value cannot be assigned again , only declaration can be issued

const can only declare aswell as assign once only.

To read a specific Key present inside an object :

Console.log(<Container>.<Key>);

Whereas To assign -

<Container>.<Name> = 'Value';

In Array -

To print a specific value =

var array = [10 , 11 , true , false , 'hello'];

var result = array[3]; (It will print the 4th value)

To change the value -

var array[3] = 'Hello';

Console.log(<container>.length)
TO KNOW THE TOTAL LENGTH OF AN ARRAY

function execute() {
     console.log(Print this)
}
(This command will print the value written inside the bracket , no need to mention the container)
called function declaration
function execute() {
     console.log(Print this , <container>)
}
(This command is used to print a parent scope value along with a internal scope value)

function execute() {
    var <container> = 10;
     console.log(Print this , <container>)
}
(Value can also be declared inside the functional scope)

WHEN ! IS USED BEFORE A CONTAINER NAME , IT CHANGES THE BOOLEAN VALUE .
LIKE TRUE TO FALSE AND FALSE TO TRUE

when 

RECOMMENDED
var val;
var = 11;

function var () {
    console.log(val);
    var val = 10;
}
(This will change the value only inside the functional scope , Locally.)

but,
when

var val;
val = 11;

function var () {
    console.log(val);
    val = 10;
}
(This will change the value in the whole script , globally.)
(Even when value is reassigned , if the function is called , like var() , then it will again be assigned. )

in const -

function var () {
    const val = 10;
    console.log(val);
}
(This cannot be reassigned)

Let is same as var.

NOTE : ALWAYS REMEMBER TO CALL THE VALUE FOR THE RESULT , OTHERWISE IT WILL NOT CONSIDER IT.

var stra = 'hello';
var strb = 'this';
var strc = 'is';
var strd = 'a';
var stre = 'sentence';
var strf = 'string';

var Total = stra + ' ' + strb + ' ' + strc + ' ' + strd + ' ' + stre + ' ' + strf + ' ' ; (Manually add spaces between words)
OR
var Total = ` ${stra} ${strb} ${strc} ${strd} ${stre} ${strf} `; (Automatically add spaces between words)
OR
var Total = ` hello this is a sentence string ` (To directly write string)

By using var <container> = object.assign({} , <container>) , copy by reference can be done but changung the value of the new container will not change the value of the previous one or can also be described as a clone of the previous container.

<container2>.<key>.push(place value eg 0)

TO SOLVE THE COPY BY REFERNECE PROBLEM IN OBJECT.ASSIGN USE THIS -

var <container2> = object.assign({} , <container1> {
    <key>: [container1.key[0] , mall.levels[1]]
})

object.assign is shallow copy

to make deep copy -

var <container2> = JSON.stringify(container1); {TO CONVERT OBJECT INTO STRING}

var <container2> = JSON.parse(container1); {TO CONVERT STRING INTO OBJECT}

SHORTHAND - 

var <container2> = JSON.parse(JSON.stringify(container1));

var <container2> = {...<container1>}
USED IN ES6 TO CLONE KEY

var <container2> = {...<container1>, <key>: [...<container1>.<key>]}

TO ASSIGN ALL THE KEYS AND VALUES FROM AN OBJECT TO ANOTHER CONTAINER , USE THIS ;

const [all the keys] = <container from which you want to copy>

for example - const { name, location, outlets, escalator, parking } = mall;

 
