# Programming Language Design Assignment #7

To TA:
這是MD檔匯出的格式，Code絕非截圖

## Delegation
1. 
	- `inheritance`: 繼承，一個child object基於parent object的架構，可以去做一些方法與性質的更改或增加
	- `delegation`: 一個object本身的方法或性質，透過另外一個object，去做方法或性質的更改或增加，與`inheritance`最大的不同就是，與另外一個object沒有上下階層的關係
2. 
	```java
	class exercise {
		String name = "exercise";
		void print(String name){
			System.out.println("I go to gym to " + name);
		}
	}
	class workout {
		String name = "work out";
		exercise object = new exercise();
		void print(){
			object.print(this.name);
		}
	}
	public class delegation{

		 public static void main(String []args){
			workout w = new workout();
			w.print();
		 }
	}
	```
## Polymorphism and Types
1. ad-hoc polymorphism
2. parametric polymorphism
3. Subtyping polymorphism
4. Structural typing
5. Nominal typing
	 - 創造rect和circle共同的parent type，裡面有一個method叫做distance_from_origin，並讓rect circle 繼承，讓rect <: [type] & circle <: [type]
6. Yes,
	Topping >: Pineapple and Hawaiian <: Pizza
	Thus, Topping→Hawaiian <: Pineaplle→Pizza
7. 
	```java
	class Animal {};
	class Cat extends Animal{};
	class Dog extends Animal{};
	class Fox extends Animal{};
	
	void talk(Cat cat) {
		System.out.println("meow meow meow");
	}
	
	void talk(Dog dog) {
		System.out.println("woof woof woof");
	}
	
	void talk(Fox fox) {
		System.out.println("");
	}
	```