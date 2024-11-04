class Cat:
    def __init__(self, name, age, breed):
        self.name = name
        self.age = age
        self.breed = breed
        self.energy = 100
        self.hunger = 0

    def meow(self):
        print(f"{self.name} каже: Мяу!")

    def sleep(self, hours):
        self.energy += hours * 10
        if self.energy > 100:
            self.energy = 100
        print(f"{self.name} спить {hours} годин і тепер має {self.energy} енергії.")

    def eat(self, food_amount):
        self.hunger -= food_amount
        if self.hunger < 0:
            self.hunger = 0
        self.energy += food_amount * 2
        if self.energy > 100:
            self.energy = 100
        print(f"{self.name} їсть {food_amount} грамів їжі і тепер має {self.hunger} голоду та {self.energy} енергії.")

    def play(self, minutes):
        self.energy -= minutes * 5
        if self.energy < 0:
            self.energy = 0
        self.hunger += minutes * 2
        if self.hunger > 100:
            self.hunger = 100
        print(f"{self.name} грається {minutes} хвилин і тепер має {self.energy} енергії та {self.hunger} голоду.")

my_cat = Cat("Мурчик", 2, "Сіамський")
my_cat.meow()
my_cat.play(10)
my_cat.eat(20)
my_cat.sleep(5)
