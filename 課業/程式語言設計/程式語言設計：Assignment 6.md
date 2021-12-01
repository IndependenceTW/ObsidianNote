# Programming Language Design Assignment #6

To TA:
這是MD檔匯出的格式，Code絕非截圖

## Multiple Inheritance
```cpp
class ios {};

class istream : public ios {
  public:
    char read_char() {};

};

class ostream : public ios {
  public:
    void print_ch(char x) {};
};

class iostream : public istream, public ostream{
};

```
## Prototype-based OOP
1.
```javascript
var Penguin = Object.create(Bird);
Penguin.name = "Penguin";
Penguin.fly = function(where){
	console.log(this.name + " can't fly.");
};
```
2.
```javascript
var Duck = Object.create(Bird);
Duck.name = "Duck";
Duck.quack = function(){
	console.log(this.name + ": can't fly.);
};
```

## Interface
```java
interface Vehicle{
	changeGear(int gear);
	speedUp(int increasedSpeed);
	applyBrakes(int decreasedSpeed);
};

class Motorcycle implement Vehicle {
	int speed = 0;
	int gear = 1;
	
	changeGear(int gear) {
		if(gear < 0) {
			gear -= 1;
		}
		if(value > 0) {
			gear += 1;
		}
	}
	
	speedUp(in increasedSpeed) {
		speed += increasedSpeed; 
	}
	
	applyBrakes(int decreasedSpeed) {
		speed -= decreasedSpeed;
	}
};

class Car implement Vehicle {
	int speed = 0;
	int gear = 1;
	bool isAcOpen = false;
	
	changeGear(int gear) {
		this.gear = gear;
	}
	
	speedUp(in increasedSpeed) {
		speed += increasedSpeed; 
	}
	
	applyBrakes(int decreasedSpeed) {
		speed -= decreasedSpeed;
	}
	
	setAirConditioner(){
		isAcOpen = !isAcOpen;
	}
};
```

