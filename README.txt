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

.......................................................................................
THE BOREDLESS TOURIST

destinations = ["Paris, France", "Shanghai, China", "Los Angeles, USA", "Sao Paulo, Brazil", "Cairo, Egypt"]
test_traveler = ['Erin Wilkes', 'Shanghai, China', ['historical site', 'art']]

def get_destination_index(destination):
  destination_index = destinations.index(destination)
  return destination_index

def get_traveler_location(traveler):
  traveler_destination = traveler[1]
  traveler_destination_index = get_destination_index(traveler_destination)
  return traveler_destination_index

test_destination_index = get_traveler_location(test_traveler)
print(test_destination_index)

attractions = [[] for destination in destinations]

def add_attraction(destination, attraction):
  try:
    destination_index = get_destination_index(destination)
    attractions_for_destination = attractions[destination_index].append(attraction)
  except SyntaxError:
    return
    
add_attraction("Los Angeles, USA", ['Venice Beach', ['beach']])
add_attraction("Paris, France", ["the Louvre", ["art", "museum"]])
add_attraction("Paris, France", ["Arc de Triomphe", ["historical site", "monument"]])
add_attraction("Shanghai, China", ["Yu Garden", ["garden", "historcical site"]])
add_attraction("Shanghai, China", ["Yuz Museum", ["art", "museum"]])
add_attraction("Shanghai, China", ["Oriental Pearl Tower", ["skyscraper", "viewing deck"]])
add_attraction("Los Angeles, USA", ["LACMA", ["art", "museum"]])
add_attraction("Sao Paulo, Brazil", ["Sao Paulo Zoo", ["zoo"]])
add_attraction("Sao Paulo, Brazil", ["Pátio do Colégio", ["historical site"]])
add_attraction("Cairo, Egypt", ["Pyramids of Giza", ["monument", "historical site"]])
add_attraction("Cairo, Egypt", ["Egyptian Museum", ["museum"]])

def find_attractions(destination, interests):
  destination_index = get_destination_index(destination)
  attractions_in_city = attractions[destination_index]
  attractions_with_interest = []
  
  for attraction in attractions_in_city:
    possible_attraction = attraction
    attraction_tags = attraction[1]
    
    for interest in interests:
      if interest in attraction_tags:
        attractions_with_interest.append(possible_attraction[0])
  return attractions_with_interest

def get_attractions_for_traveler(traveler):
  traveler_destination = traveler[1]
  traveler_interest = traveler[2]
  traveler_attractions = find_attractions(traveler_destination, traveler_interest)
  interest_string = "Hi "+ traveler[0] + ", we think you'll like these places around "
  
  for i in range(len(traveler_attractions)):
    if traveler_attractions[-1] == traveler_attractions[i]:
      interest_string += "the " + traveler_attractions[i] + "."
    else:
      interest_string += "the " + traveler_attractions[i] + ", "
  return interest_string

smills_france = get_attractions_for_traveler(['Dereck Smill', 'Paris, France', ['monument']])

print(smills_france)

......................................................................................
THREAD SHED

daily_sales = \
"""Edith Mcbride   ;,;$1.21   ;,;   white ;,; 
09/15/17   ,Herbert Tran   ;,;   $7.29;,; 
white&blue;,;   09/15/17 ,Paul Clarke ;,;$12.52 
;,;   white&blue ;,; 09/15/17 ,Lucille Caldwell   
;,;   $5.13   ;,; white   ;,; 09/15/17,
Eduardo George   ;,;$20.39;,; white&yellow 
;,;09/15/17   ,   Danny Mclaughlin;,;$30.82;,;   
purple ;,;09/15/17 ,Stacy Vargas;,; $1.85   ;,; 
purple&yellow ;,;09/15/17,   Shaun Brock;,; 
$17.98;,;purple&yellow ;,; 09/15/17 , 
Erick Harper ;,;$17.41;,; blue ;,; 09/15/17, 
Michelle Howell ;,;$28.59;,; blue;,;   09/15/17   , 
Carroll Boyd;,; $14.51;,;   purple&blue   ;,;   
09/15/17   , Teresa Carter   ;,; $19.64 ;,; 
white;,;09/15/17   ,   Jacob Kennedy ;,; $11.40   
;,; white&red   ;,; 09/15/17, Craig Chambers;,; 
$8.79 ;,; white&blue&red   ;,;09/15/17   , Peggy Bell;,; $8.65 ;,;blue   ;,; 09/15/17,   Kenneth Cunningham ;,;   $10.53;,;   green&blue   ;,; 
09/15/17   ,   Marvin Morgan;,;   $16.49;,; 
green&blue&red   ;,;   09/15/17 ,Marjorie Russell 
;,; $6.55 ;,;   green&blue&red;,;   09/15/17 ,
Israel Cummings;,;   $11.86   ;,;black;,;  
09/15/17,   June Doyle   ;,;   $22.29 ;,;  
black&yellow ;,;09/15/17 , Jaime Buchanan   ;,;   
$8.35;,;   white&black&yellow   ;,;   09/15/17,   
Rhonda Farmer;,;$2.91 ;,;   white&black&yellow   
;,;09/15/17, Darren Mckenzie ;,;$22.94;,;green 
;,;09/15/17,Rufus Malone;,;$4.70   ;,; green&yellow 
;,; 09/15/17   ,Hubert Miles;,;   $3.59   
;,;green&yellow&blue;,;   09/15/17   , Joseph Bridges  ;,;$5.66   ;,; green&yellow&purple&blue 
;,;   09/15/17 , Sergio Murphy   ;,;$17.51   ;,;   
black   ;,;   09/15/17 , Audrey Ferguson ;,; 
$5.54;,;black&blue   ;,;09/15/17 ,Edna Williams ;,; 
$17.13;,; black&blue;,;   09/15/17,   Randy Fleming;,;   $21.13 ;,;black ;,;09/15/17 ,Elisa Hart;,; $0.35   ;,; black&purple;,;   09/15/17   ,
Ernesto Hunt ;,; $13.91   ;,;   black&purple ;,;   
09/15/17,   Shannon Chavez   ;,;$19.26   ;,; 
yellow;,; 09/15/17   , Sammy Cain;,; $5.45;,;   
yellow&red ;,;09/15/17 ,   Steven Reeves ;,;$5.50   
;,;   yellow;,;   09/15/17, Ruben Jones   ;,; 
$14.56 ;,;   yellow&blue;,;09/15/17 , Essie Hansen;,;   $7.33   ;,;   yellow&blue&red
;,; 09/15/17   ,   Rene Hardy   ;,; $20.22   ;,; 
black ;,;   09/15/17 ,   Lucy Snyder   ;,; $8.67   
;,;black&red  ;,; 09/15/17 ,Dallas Obrien ;,;   
$8.31;,;   black&red ;,;   09/15/17,   Stacey Payne 
;,;   $15.70   ;,;   white&black&red ;,;09/15/17   
,   Tanya Cox   ;,;   $6.74   ;,;yellow   ;,; 
09/15/17 , Melody Moran ;,;   $30.84   
;,;yellow&black;,;   09/15/17 , Louise Becker   ;,; 
$12.31 ;,; green&yellow&black;,;   09/15/17 ,
Ryan Webster;,;$2.94 ;,; yellow ;,; 09/15/17 
,Justin Blake ;,; $22.46   ;,;white&yellow ;,;   
09/15/17,   Beverly Baldwin ;,;   $6.60;,;   
white&yellow&black ;,;09/15/17   ,   Dale Brady   
;,;   $6.27 ;,; yellow   ;,;09/15/17 ,Guadalupe Potter ;,;$21.12   ;,; yellow;,; 09/15/17   , 
Desiree Butler ;,;$2.10   ;,;white;,; 09/15/17  
,Sonja Barnett ;,; $14.22 ;,;white&black;,;   
09/15/17, Angelica Garza;,;$11.60;,;white&black   
;,;   09/15/17   ,   Jamie Welch   ;,; $25.27   ;,; 
white&black&red ;,;09/15/17   ,   Rex Hudson   
;,;$8.26;,;   purple;,; 09/15/17 ,   Nadine Gibbs 
;,;   $30.80 ;,;   purple&yellow   ;,; 09/15/17   , 
Hannah Pratt;,;   $22.61   ;,;   purple&yellow   
;,;09/15/17,Gayle Richards;,;$22.19 ;,; 
green&purple&yellow ;,;09/15/17   ,Stanley Holland 
;,; $7.47   ;,; red ;,; 09/15/17 , Anna Dean;,;$5.49 ;,; yellow&red ;,;   09/15/17   ,
Terrance Saunders ;,;   $23.70  ;,;green&yellow&red 
;,; 09/15/17 ,   Brandi Zimmerman ;,; $26.66 ;,; 
red   ;,;09/15/17 ,Guadalupe Freeman ;,; $25.95;,; 
green&red ;,;   09/15/17   ,Irving Patterson 
;,;$19.55 ;,; green&white&red ;,;   09/15/17 ,Karl Ross;,;   $15.68;,;   white ;,;   09/15/17 , Brandy Cortez ;,;$23.57;,;   white&red   ;,;09/15/17, 
Mamie Riley   ;,;$29.32;,; purple;,;09/15/17 ,Mike Thornton   ;,; $26.44 ;,;   purple   ;,; 09/15/17, 
Jamie Vaughn   ;,; $17.24;,;green ;,; 09/15/17   , 
Noah Day ;,;   $8.49   ;,;green   ;,;09/15/17   
,Josephine Keller ;,;$13.10 ;,;green;,;   09/15/17 ,   Tracey Wolfe;,;$20.39 ;,; red   ;,; 09/15/17 ,
Ignacio Parks;,;$14.70   ;,; white&red ;,;09/15/17 
, Beatrice Newman ;,;$22.45   ;,;white&purple&red 
;,;   09/15/17, Andre Norris   ;,;   $28.46   ;,;   
red;,;   09/15/17 ,   Albert Lewis ;,; $23.89;,;   
black&red;,; 09/15/17,   Javier Bailey   ;,;   
$24.49   ;,; black&red ;,; 09/15/17   , Everett Lyons ;,;$1.81;,;   black&red ;,; 09/15/17 ,   
Abraham Maxwell;,; $6.81   ;,;green;,;   09/15/17   
,   Traci Craig ;,;$0.65;,; green&yellow;,; 
09/15/17 , Jeffrey Jenkins   ;,;$26.45;,; 
green&yellow&blue   ;,;   09/15/17,   Merle Wilson 
;,;   $7.69 ;,; purple;,; 09/15/17,Janis Franklin   
;,;$8.74   ;,; purple&black   ;,;09/15/17 ,  
Leonard Guerrero ;,;   $1.86   ;,;yellow  
;,;09/15/17,Lana Sanchez;,;$14.75   ;,; yellow;,;   
09/15/17   ,Donna Ball ;,; $28.10  ;,; 
yellow&blue;,;   09/15/17   , Terrell Barber   ;,; 
$9.91   ;,; green ;,;09/15/17   ,Jody Flores;,; 
$16.34 ;,; green ;,;   09/15/17,   Daryl Herrera 
;,;$27.57;,; white;,;   09/15/17   , Miguel Mcguire;,;$5.25;,; white&blue   ;,;   09/15/17 ,   
Rogelio Gonzalez;,; $9.51;,;   white&black&blue   
;,;   09/15/17   ,   Lora Hammond ;,;$20.56 ;,; 
green;,;   09/15/17,Owen Ward;,; $21.64   ;,;   
green&yellow;,;09/15/17,Malcolm Morales ;,;   
$24.99   ;,;   green&yellow&black;,; 09/15/17 ,   
Eric Mcdaniel ;,;$29.70;,; green ;,; 09/15/17 
,Madeline Estrada;,;   $15.52;,;green;,;   09/15/17 
, Leticia Manning;,;$15.70 ;,; green&purple;,; 
09/15/17 ,   Mario Wallace ;,; $12.36 ;,;green ;,; 
09/15/17,Lewis Glover;,;   $13.66   ;,;   
green&white;,;09/15/17,   Gail Phelps   ;,;$30.52   
;,; green&white&blue   ;,; 09/15/17 , Myrtle Morris 
;,;   $22.66   ;,; green&white&blue;,;09/15/17"""

#------------------------------------------------
# Start coding below!
#Replace ;,; with : in string to make it more legible.
daily_sales_replaced = daily_sales.replace(';,;',':' )
#Split the daily sales separated with a comma.
daily_transactions = daily_sales_replaced.split(',')
#splitting each sales into it's own list
daily_transactions_split = []
for sales in daily_transactions:
    daily_transactions_split.append(sales.split(':'))

transactions_clean = []
for each_sales in daily_transactions_split:
    transaction_clean = []
    for sales in each_sales:
        transaction_clean.append(sales.replace('\n', '').strip(" "))
    transactions_clean.append(transaction_clean)

customers = []
sales = []
thread_sold = []
for sales_data in transactions_clean:
    customers.append(sales_data[0])
    sales.append(sales_data[1])
    thread_sold.append(sales_data[2])

#Determine the total value of the days sales.
total_sales = 0
for amount in sales:
    total_sales += float(amount.strip('$'))
#print(total_sales)

#How much thread of any specific color was sold?
thread_sold_split = []
for thread in thread_sold:
  for colour in thread.split("&"):
    thread_sold_split.append(colour)
#print(thread_sold_split)

def count_colour(colour):
    colour_count = 0
    for thread_colour in thread_sold_split:
        if colour == thread_colour:
            colour_count += 1
    return colour_count

#print(count_colour('white'))

colors = ['red','yellow','green','white','black','blue','purple']

def count_colour(colors):
    count = 0
    for colour in thread_sold_split:
        if colors == colour:
            count += 1
    return 'Thread Shed sold {} threads of {} thread today.'.format(count, colors)

print(count_colour('blue'))

......................................................................................
SCRABBLE SCORE

letters = ["A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V",
           "W", "X", "Y", "Z"]
points = [1, 3, 3, 2, 1, 4, 2, 4, 1, 8, 5, 1, 3, 4, 1, 3, 10, 1, 1, 1, 1, 4, 4, 8, 4, 10]

letter_to_points = {key: value for key, value in zip(letters, points)}

letter_to_points.update({"": 0})


# print(letter_to_points)

def score_word(word):
    point_total = 0
    for letter in word:
        if letter in letter_to_points:
            point_total += letter_to_points[letter]
        else:
            point_total += 0
    return point_total


brownie_points = score_word("BROWNIE")
# print(brownie_points)

player_to_words = {"player1": ["BLUE", "TENNIS", "EXIT"], "wordNerd": ["EARTH", "EYES", "MACHINE"],
                   "lexi Con": ["ERASER", "BELLY", "HUSKY"], "Prof Reader": ["ZAP", "COMA", "PERIOD"]}

player_to_points = {}
for key, word in player_to_words.items():
    player = key
    words = word
    player_points = 0
    for word_spell in words:
        player_points += score_word(word_spell)
        player_to_points[player] = player_points
print(player_to_points)






