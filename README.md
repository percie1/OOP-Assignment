# OOP-Assignment

# Parent class
class Superhero:
    def __init__(self, name, power, city):
        self.name = name
        self.power = power
        self._city = city  # protected attribute (encapsulation)

    def introduce(self):
        print(f"I am {self.name}, protector of {self._city}!")

    def use_power(self):
        print(f"{self.name} uses {self.power}!")

# Subclass (inheritance + polymorphism)
class FlyingHero(Superhero):
    def use_power(self):
        print(f"{self.name} soars through the sky with {self.power}! 🕊️")

# Another subclass
class TechHero(Superhero):
    def use_power(self):
        print(f"{self.name} activates tech gear: {self.power}! 🤖")

# Creating objects
hero1 = FlyingHero("SkyFlash", "Flight", "Sky City")
hero2 = TechHero("ByteBlade", "Cyber Armor", "Tech Town")

# Test the classes
hero1.introduce()
hero1.use_power()
hero2.introduce()
hero2.use_power()



class Vehicle:
    def move(self):
        print("The vehicle moves.")

class Car(Vehicle):
    def move(self):
        print("Driving on the road! 🚗")

class Plane(Vehicle):
    def move(self):
        print("Flying through the sky! ✈️")

class Boat(Vehicle):
    def move(self):
        print("Sailing across the sea! 🚤")

# Polymorphism in action
vehicles = [Car(), Plane(), Boat()]

for v in vehicles:
    v.move()
