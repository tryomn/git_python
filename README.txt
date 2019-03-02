def repeat_stuff(stuff, num_repeats=10):
  return stuff*num_repeats

lyrics = repeat_stuff("Row ", 3) + "Your Boat. "
song = repeat_stuff(lyrics)

print(song)

..............................................................................

train_mass = 22680
train_acceleration = 10
train_distance = 100

bomb_mass = 1

# Temperature conversion from Fahrenhiet to Celsius
def f_to_c(f_temp, c_temp = 0):
# Conversion formular
	c_temp = (f_temp - 32)*5/9
	return c_temp
f100_in_celsius = f_to_c(100)
c_temp = f100_in_celsius
print("The celsius equivalent of 100 Fahrenhiet:" + " " + str(c_temp))

# Temperature conversion from Celsius to Fahrenhiet
def c_to_f(c_temp, f_temp = 0):
  # Conversion Formular
  f_temp = c_temp * (9/5) +32
  return f_temp
c0_in_fahrenheit = c_to_f(0)
f_temp = c0_in_fahrenheit
print("The Fahreheit equivalent of 0 celsius:" + " " + str(f_temp))

# Defining a function call force
def get_force(mass, acceleration):
	return mass*acceleration
train_force = get_force(train_mass, train_acceleration)
print("The GE train supplies" + " " + str(train_force) + " " + "Newtons of force.")

# Defining a function called energy
# C is a constant that is usually set to the speed of light which is roughly 3*10^8
c = 3*10**8
def get_energy(mass, c):
  return mass*c**2
bomb_energy = get_energy(1, c)
print("A 1kg bomb supplies" + " " + str(bomb_energy) + "joules")

# Defining function for work
def get_work(mass, acceleration, distance):
  force = mass*acceleration
  return force*distance
train_work = get_work(train_mass, train_acceleration, train_distance)
print("The GE train does " + " "+ str(train_work) + "joules of work over" + " " + str(train_distance) + "meters.")

..............................................................................
# lovely loveseat for neat suites on fleet street, description
lovely_loveseat_description = """Lovely loveseat. Tufted polyester blend on wood. 32 inches high x 40 inches wide x 30 inches deep. Red and white."""

# price listing for the lovely loveseat items
lovely_loveseat_price = 254.00

# Stylish settee inventory
stylish_settee_description = "Stylish settee. faux leather on bitch. 29.50 inches x 54.74 inches wide x 28 inches deep. black."
# price listing for the lovely loveseat items
stylish_settee_price = 180.50

# Luxuriou lamp inventory
luxurious_lamp_description = "Luxurious lamp. Glass and iron. 36 inches tall. Brown with cream shade."

# price listing for Luxurious lamp, glass iron and brown cream shade
luxurious_lamp_price = 52.15

# Sales tax
sales_tax = 0.088

# Customer Sales
customer_one_total = 0

# Customer listing
customer_one_itemization = ""

# Customer one started purchase
customer_one_total += lovely_loveseat_price
customer_one_total += luxurious_lamp_price
customer_one_itemization = lovely_loveseat_description + luxurious_lamp_description

# Sales Tax
customer_one_tax = customer_one_total*sales_tax
customer_one_total += customer_one_tax
print(customer_one_itemization)

# Customer one total cost
print("Customer_one_total:" +" " +str(customer_one_total))

..............................................................................
ABOUT GIT

Quick setup — if you’ve done this kind of thing before
or HTTPS/SSH : https://github.com/tryomn/git_practice.git

Get started by creating a new file or uploading an existing file. We recommend every repository include a README, LICENSE, and .gitignore.
…or create a new repository on the command line

echo "# git_practice" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/tryomn/git_practice.git
git push -u origin master

…or push an existing repository from the command line

git remote add origin https://github.com/tryomn/git_practice.git
git push -u origin master

..............................................................................
def graduation_reqs(gpa, credits):
  if (gpa >= 2.0) and (credits >= 120):
    return "You meet the requirements to graduate!"
  if (gpa >= 2.0) and not (credits >= 120):
    return "You do not have enough credits to graduate."
  if not (gpa >= 2.0) and (credits >= 120):
    return "Your GPA is not high enough to graduate."
  else:
    return "You do not meet the GPA or the credit requirement for graduation."
.............................................................................
def divide_two_numbers(x, y):
  result = x / y
  return result

try:
  result = divide_two_numbers(2,0)
  print(result)
except NameError:
  print("A NameError occurred.")
except ValueError:
  print("A ValueError occurred.") 
except ZeroDivisionError:
  print("A ZeroDivisionError occurred.")

..............................................................................
SAL'S SHIPPING

# Sal's Shipping; Shipping cost ground
def shipping_cost_ground(weight):
  if weight <= 2:
    price_per_pound = 1.50
  elif weight <= 6:
    price_per_pound = 3.00
  elif weight <= 10.0:
  	price_per_pound = 4.00
  else:
    price_per_pound = 4.75
    
  return 20 + (price_per_pound * weight)
  
print(shipping_cost_ground(8.4))

shipping_cost_premium = 125.0


def shipping_cost_drone(weight):
  if weight <= 2:
    price_per_pound = 4.50
  elif weight <= 6:
    price_per_pound = 9.00
  elif weight <= 10.0:
  	price_per_pound = 12.00
  else:
    price_per_pound = 14.25
    
  return (price_per_pound * weight)

print(shipping_cost_drone(1.5))

def print_cheapest_shipping_method(weight):
  
  ground = shipping_cost_ground(weight)
  premium = shipping_cost_premium
  drone = shipping_cost_drone(weight)
  
  if ground < premium and ground < drone:
    method = "Standard ground"
    cost = ground
  elif premium < ground and premium < drone:
    method = "Premium ground"
    cost = premium
  else:
    method = "drone"
    cost = drone
  
  print(
  "The cheapest option available is $%.2f with %s shipping."
  % (cost, method)
  )
  
print_cheapest_shipping_method(4.8)
print_cheapest_shipping_method(41.5)

..............................................................................
GRADEBOOK

subjects = ['physics', 'calculus', 'poetry', 'history']
grades = [98, 97, 85, 88]

subjects.append('computer science')
grades.append(100)

gradebook = zip(subjects, grades)

subjects.append('visual arts')
grades.append(93)

last_semester_gradebook = [('physics', 90), ('calculus', 94), ('poetry', 95), ('history', 89), ('computer science', 100), ('visual arts', 96)]

full_gradebook = zip(last_semester_gradebook, gradebook)

print(list(full_gradebook))

..............................................................................
Lens Slice
# Len's Slice pizza joint
toppings = ['pepperoni', 'pineapple', 'cheese', 'sausage', 'olives', 'anchovies', 'mushrooms']
prices = [2, 6, 1, 3, 2, 7, 2]
# Length of toppings
num_pizzas = len(toppings)
print("We sell %.0f different kinds of pizza!"
     %(num_pizzas)
     )
pizzas = list(zip(prices, toppings))

#Sorting and Slicing pizzas
pizzas.sort()

print(pizzas)

cheapest_pizza = pizzas[0]
priciest_pizza = pizzas[-1]
three_cheapest = pizzas[:3]
..............................................................................
SUMMING A LIST

def listsum(numList):
   if len(numList) == 1:
        return numList[0]
   else:
        return numList[0] + listsum(numList[1:])

print(listsum([1,3,5,7,9]))

..............................................................................
Python Loops
Carly's Clippers

hairstyles = ["bouffant", "pixie", "dreadlocks", "crew", "bowl", "bob", "mohawk", "flattop"]

prices = [30, 25, 40, 20, 20, 35, 50, 35]

last_week = [2, 3, 5, 8, 4, 4, 6, 2]


total_prices = 0

for i in prices:
  total_prices += i
print(total_prices)
average_price = total_prices/len(prices)
print(" The average haircut prices is " + str(average_price))

new_prices = [ i - 5 for i in prices]
print(new_prices)

total_revenue = 0
for i in range(len(hairstyles)):
  total_revenue = prices[i] * last_week[i]
print("Total revenue: " + str(total_revenue))

average_daily_revenue = total_revenue/7
print(average_daily_revenue)

cuts_under_30 = []

for i in new_prices:
  if i < 30:
    cuts_under_30.append(i)
    print(cuts_under_30)
