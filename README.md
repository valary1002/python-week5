ACTIVITY 1
# Base class: Smartphone
class Smartphone:
    def __init__(self, brand, model, storage):
        self.brand = brand
        self.model = model
        self.storage = storage
    
    def display_info(self):
        return f"Brand: {self.brand}, Model: {self.model}, Storage: {self.storage}GB"
    
    def make_call(self, number):
        return f"Calling {number} from {self.model}..."

# Inherited class: SmartphoneWithCamera
class SmartphoneWithCamera(Smartphone):
    def __init__(self, brand, model, storage, camera_quality):
        super().__init__(brand, model, storage)
        self.camera_quality = camera_quality
    
    def take_picture(self):
        return f"Taking a picture with {self.camera_quality} MP camera..."

# Create objects
phone1 = Smartphone("Samsung", "Galaxy S21", 128)
phone2 = SmartphoneWithCamera("Apple", "iPhone 13", 256, 12)

# Using methods
print(phone1.display_info())
print(phone1.make_call("123-456-7890"))
print(phone2.display_info())
print(phone2.take_picture())

ACTIVITY 2
# Base class: Animal
class Animal:
    def move(self):
        return "The animal moves..."

# Derived class: Dog
class Dog(Animal):
    def move(self):
        return "The dog runs..."

# Derived class: Bird
class Bird(Animal):
    def move(self):
        return "The bird flies..."

# Base class: Vehicle
class Vehicle:
    def move(self):
        return "The vehicle moves..."

# Derived class: Car
class Car(Vehicle):
    def move(self):
        return "The car drives... 🚗"

# Derived class: Plane
class Plane(Vehicle):
    def move(self):
        return "The plane flies... ✈️"

# Testing the polymorphism
animals = [Dog(), Bird()]
vehicles = [Car(), Plane()]

# Call the move() method for each
for animal in animals:
    print(animal.move())

for vehicle in vehicles:
    print(vehicle.move())
