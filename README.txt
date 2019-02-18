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
