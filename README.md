1、对象篇
1、对象获取值：                                                 
 获取值
例如1：
        var testObj = {
          "an entree": "hamburger",
          "my side": "veggies",
          "the drink": "water"
        };


        var entreeValue = testObj["an entree"];   
        var drinkValue = testObj["the drink"];  


例如2：
        var testObj = {
          "entree": "hamburger",
          "side": "veggies",
          "drink": "water"
        };


        var entreeValue = testObj.entree;
        var drinkValue = testObj.drink;

例如3：
        var myDog = "Hunter";
        var dogs = {
          Fido: "Mutt",
          Hunter: "Doberman",
          Snoopie: "Beagle"
        }
        var breed = dogs[myDog]; // "Hunter"
        console.log(breed)// "Doberman"


2、修改对象里面值：                                          
  修改值

举个例子，让我们看看 ourDog:
          var ourDog = {
            "name": "Camper",
            "legs": 4,
            "tails": 1,
            "friends": ["everything!"]
          };
         让我们更改它的name名称为 "Happy Camper"，这有两种方式来更新对象的name属性：

ourDog.name = "Happy Camper";

ourDog["name"] = "Happy Camper";

例如5：添加对象属性                                              
         添加值
        var ourDog = {
          "name": "Camper",
          "legs": 4,
          "tails": 1,
          "friends": ["everything!"]
        };
      看看我们是如何给ourDog添加 "bark"属性：

       ourDog.bark = "bow-wow";

       或者

       ourDog["bark"] = "bow-wow";

例如6：   删除对象在值                                           
           
           删除值
        var ourDog = {
          "name": "Camper",
          "legs": 4,
          "tails": 1,
          "friends": ["everything!"],
          "bark": "bow-wow"
        };

      我们同样可以删除对象的属性，例如：

       delete ourDog.bark;



取值：  switch case 替换这个。
这是简单的反向字母表：

          var alpha = {
            1:"Z",
            2:"Y",
            3:"X",
            4:"W",
            ...
            24:"C",
            25:"B",
            26:"A"
          };
          alpha[2]; // "Y"
          alpha[24]; // "C"

          var value = 2;
          alpha[value]; // "Y"


检查对象属性是否存在：我们可以用.hasOwnProperty(propname)方法来检查对象是否有该属性。如果有返回true，反之返回 false。

举例

        var myObj = {
          top: "hat",
          bottom: "pants"
        };
        myObj.hasOwnProperty("top");    // true
        myObj.hasOwnProperty("middle"); // false


获取嵌套对象的值：
下面是一个嵌套的JSON对象：

            var ourStorage = {
              "desk": {
                "drawer": "stapler"
              },
              "cabinet": {
                "top drawer": { 
                  "folder1": "a file",
                  "folder2": "secrets"
                },
                "bottom drawer": "soda"
              }
            }
            ourStorage.cabinet["top drawer"].folder2;  // "secrets"
            ourStorage.desk.drawer; // "stapler"


例如：
            var collection = {
                2548: {
                  album: "Slippery When Wet",
                  artist: "Bon Jovi",
                  tracks: [ 
                    "Let It Rock", 
                    "You Give Love a Bad Name" 
                  ]
                },
                2468: {
                  album: "1999",
                  artist: "Prince",
                  tracks: [ 
                    "1999", 
                    "Little Red Corvette" 
                  ]
                },
                1245: {
                  artist: "Robert Palmer",
                  tracks: [ ]
                },
                5439: {
                  album: "ABBA Gold"
                }
            };
         var collectionCopy = JSON.parse(JSON.stringify(collection));
      写一个函数，它有个三个参数，id、prop、 value。

如果 value !='' 而且prop != 'tracks' ，collectionCopy[id][prop]=value;。 添加值

如果 value !='' 而且prop == 'tracks' ，collectionCopy[id][prop].push(value);。   添加到最后面

如果 value == '' ，delete collectionCopy[id][prop];。删除值

记住：函数返回的永远是整个对象。





