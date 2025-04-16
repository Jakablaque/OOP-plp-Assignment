# OOP-plp-Assignment
Create a class representing anything you like (a Smartphone, Book, or even a Superhero!).
Add attributes and methods to bring the class to life!
Use constructors to initialize each object with unique values.
Add an inheritance layer to explore polymorphism or encapsulation.
Activity 2: Polymorphism Challenge! 🎭

Create a program that includes animals or vehicles with the same action (like move()). However, make each class define move() differently (for example, Car.move() prints "Driving" 🚗, while Plane.move() prints "Flying" ✈️).





class Superhero:
    def __init__(self, name, power, level):
        self.name = name
        self.power = power
        self.__level = level  # Encapsulated (private) attribute

    def show_identity(self):
        return f"I am {self.name}, and I use {self.power}!"

    def get_level(self):
        return self.__level

    def level_up(self):
        self.__level += 1
        return f"{self.name} has leveled up to {self.__level}!"
#subclass with added superheroes

class FlyingSuperhero(Superhero):
    def __init__(self, name, power, level, flight_speed):
        super().__init__(name, power, level)
        self.flight_speed = flight_speed

    def fly(self):
        return f"{self.name} flies at {self.flight_speed} km/h!"

#objects
hero1 = Superhero("Boltman", "Electric Surge", 5)
hero2 = FlyingSuperhero("SkyQueen", "Wind Control", 7, 300)

print(hero1.show_identity())
print(hero1.level_up())
print(hero2.show_identity())
print(hero2.fly())



POLYMORPHISM CHALLENGE.

class Vehicle:
    def move(self):
        print("The vehicle moves.")

class Car(Vehicle):
    def move(self):
        print("Driving on the road 🚗")

class Plane(Vehicle):
    def move(self):
        print("Flying in the sky ✈️")

class Boat(Vehicle):
    def move(self):
        print("Sailing on the water ⛵")

# Test polymorphism
vehicles = [Car(), Plane(), Boat()]

for v in vehicles:
    v.move()

