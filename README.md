# python-exploration

my_name = "Jenni"
print("Hello and welcome " + my_name + "!")
print('Hello world!')

cars = 100
space_in_a_car = 4.0
drivers = 30
passengers = 90
cars_not_driven= cars - drivers
cars_driven = drivers
carpool_capacity = cars_driven * space_in_a_car
average_passengers_per_car = passengers / cars_driven

print("there are", cars, "cars available.")
print("There are only", drivers, "drivers available.")
print("There will be", cars_not_driven, "empty cars today.")
print("We can transport", carpool_capacity, "people today.")
print("We have", passengers, "to carpool today.")
print("We need to put about", average_passengers_per_car,
      "in each car.")

my_age = 31
my_hair = "brown"
my_height = 70

print(f"Let's talk about {my_name}.")
print(f"Her hair is {my_hair}")
print(f"If I add {my_age} and {my_height} I get {my_age + my_height}")


def loading_screen():
  print('This page is loading . . .')

loading_screen()

def mult_two_add_three(number):
  print(number*2 + 3)

mult_two_add_three(1)
mult_two_add_three(5)
mult_two_add_three(-1)
mult_two_add_three(0)

#refactor
def mult_x_add_y(number, x, y):
  print(number*x + y)
  
mult_x_add_y(5, 2, 3)
mult_x_add_y(1, 3, 1)

def create_spreadsheet(title, row_count = 1000):
  print("Creating a spreadsheet called " + title + " with " + str(row_count) + " rows")

create_spreadsheet(title='Applications', row_count=10)

#multiple return values
def get_boundaries(target, margin): 
  low_limit = target - margin
  high_limit = margin + target
  return low_limit, high_limit

low, high = get_boundaries(100, 20)
print(low)
print(high)

def repeat_stuff(stuff, num_repeats=10):
  return stuff*num_repeats

repeat_stuff("Row ", 3)

lyrics = repeat_stuff("Row ", 3) + "Your Boat. "

song = repeat_stuff(lyrics)

print(song)

#conditional
def dave_check(user_name):
  if user_name == "Dave":
    return "Get off my computer Dave!"
  if user_name == "angela_catlady_87":
    return "I know it is you Dave! Go away!"

  

user_name = "Jenni"

print(dave_check(user_name))

####zip keyword
names = ['Jenny', 'Alexus', 'Sam', 'Grace']
dogs_names = ['Elphonse', 'Dr. Doggy DDS', 'Carter', 'Ralph']

names_and_dogs_names = zip(names, dogs_names)

list_of_names_and_dogs_names = print(list(names_and_dogs_names))

####append
orders = ['daisies', 'periwinkle']

print(orders)

orders.append('tulips')
orders.append('roses')
print(orders)

####dictionary
animals_in_zoo = {}

animals_in_zoo['zebras'] = 8
animals_in_zoo['monkeys'] = 12
animals_in_zoo['dinosaurs'] = 0

print(animals_in_zoo)

animals_in_zoo.update({'fish': 20, 'giraffes': 5})
print(animals_in_zoo)

animals_in_zoo['fish'] = 30
print(animals_in_zoo)

####list comprehension
drinks = ["espresso", "chai", "decaf", "drip"]
caffeine = [64, 40, 0, 120]

zipped_drinks = zip(drinks, caffeine)

drinks_to_caffeine ={key:value for key, value in zipped_drinks}

print(drinks_to_caffeine)

####for loop
board_games = ['Settlers of Catan', 'Carcassone', 'Power Grid', 'Agricola', 'Scrabble']

for game in board_games:
  print(game)

####range in loop
promise = "I will not chew gum in class"

for i in range(5):
  print(promise)

####append w/ loop
students_period_A = ["Alex", "Briana", "Cheri", "Daniele"]
students_period_B = ["Dora", "Minerva", "Alexa", "Obie"]

for student in students_period_A:
  students_period_B.append(student)
  print(student)

####break
dog_breeds_available_for_adoption = ['french_bulldog', 'dalmatian', 'shihtzu', 'poodle', 'collie']
dog_breed_I_want = 'dalmatian'

for dog_breed in dog_breeds_available_for_adoption:
  print(dog_breed)
  if dog_breed == dog_breed_I_want:
    print("They have the dog I want!")
    break

####continue
ages = [12, 38, 34, 26, 21, 19, 67, 41, 17]

for i in ages:
  if i < 21:
    continue
  print(i)

####while loop
all_students = ["Alex", "Briana", "Cheri", "Daniele", "Dora", "Minerva", "Alexa", "Obie", "Arius", "Loki"]
students_in_poetry = []

while len(students_in_poetry) < 6:
  students_in_poetry.append(all_students.pop())
print(students_in_poetry)


####fizzBuzz in Python
def fizzBuzz(num):
    if num % 15 == 0:
       print('FizzBuzz')
    elif num % 3 == 0:
       print('Fizz')
    elif num % 5 == 0:
        print('Buzz')

fizzBuzz(30)
fizzBuzz(10)
fizzBuzz(6)

####Dictionary in function
def relation_to_luke(name):
	dict = {
	'Darth Vader' : 'father',
	'Leia' : 'sister',
	'Han' : 'brother in law',
	'R2D2' : 'droid'
	}
	
	return 'Luke, I am your ' + dict[name] + "."

relation_to_luke('Han')
