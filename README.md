# Final-Project
CIS 1051 Final Project
#Radhika Khandelwal
#CIS 1051 Final Project
#Holiday Train Travel Ticket Price Calculator

prices = {"Washington D.C. to Philadelphia": "", "Washington D.C. to New York City": "", "Washington D.C. to Montreal": ""}
oneticketweekdaydiscount = 10
startyear = 2021
endyear = 2022
november = 11
december = 12
january = 13
daysinmonth = 30
leap_year = 4
century = 100
daysinweek = 7

def introduction():
    print("Thank you for choosing Holiday Travels for your holiday getaway.
          "\nAll trips start from and return back to Washington D.C. and all trips nmust take place between Nov 15, 2021 and Jan 15, 2022.
          "\nWhen asked, please enter your destination, your departure/return dates, and the number of adult and child tickets you would like to purchase.
          "\nPlease be aware that at least one adult ticket must be purchased in order to purchase child tickets.
          "\nThe total cost of the tickets will be displayed.")

def destination():
    destinationinput = input("Destination: ")
    while destinationinput != "PHL" or destinationinput != "NYC" or destinationinput != "MTL":
        print("Invalid. Please try again.")
        destinationinput = input("Destination(PHL, NYC, MTL): ")

def departure():
    departuremonth = input("Departure month: ")
    departureday = input("Departure day: ")

def returns():
    returnmonth = input("Return month: ")
    returnday = input("Return day: ")
    

def discountapplication(departuremonth, returnmonth):
    if departuremonth != 1:
        year = startyear
    else:
        year = endyear
    if returnmonth != 1:
        year = startyear
    else:
        year = endyear
        
def adultticket():
    adulttickets = int(input("Number of adult tickets: "))
    while adulttickets < 0:
        print("Invalid. Please try again.")
        adulttickets = int(input("Number of adult tickets: "))
    if adulttickets == 0:
        print("price of tickets: $" + price(destination, adulttickets, childtickets, weekdaytravels) + ".00")

def childticket():
    childtickets = int(input("Number of child tickets: "))
     while childtickets < 0:
        print("Invalid. Please try again.")
        childtickets = int(input("Number of child tickets: "))

print("price of tickets: $" + price(destination, adulttickets, childtickets, weekdaytravels) + ".00")
        
def datecheck(departuremonth, departureday, daysinmonth):
    if (departuremonth == 1 and departureday > 0 and departureday < (daysinmonth / 2) + 1) or (departuremonth == november and departureday > 0 and departureday < (daysinmonth + 2)) or (departuremonth == december and departureday > 0 and departureday < (daysinmonth +2)):
        validdeparture = true
    if (returnmonth == 1 and returnday > 0 and returnday < (daysinmonth / 2) + 1) or (returnmonth == november and returnday > 0 and returnday < (daysinmonth + 1)) or (returnmonth == december and returnday > 0 and returnday < (daysinmonth+2)):
        validreturn = true
    if returnmonth == 1:
        returnmonth = january
    if departuremonth == 1:
        departuremonth == january
    if (returnmonth > departuremonth) or (returnmonth == departuremonth and returnday > departureday):
        correctmonth = true
    isvalid = validdeparture and validreturn and correctmonth
    if isvalid:
        return true
    else:
        print("Invalid. Please try again.")
        return false
    if isvalid = false:
        datecheck(departuremonth, departureday, daysinmonth)

def dayofweekofdate(december, dayofweek, daysofweek, year, month):
  a = year - ((december + 2) - month) / december
  b = a + a / leap_year - a / century + a / (century * leap_year)
  c = month + december * (((december + 2) - month)/ december) - 2
  dayofweek = (day + a + ((daysinmonth + 1) * z) / december) % daysinweek
  if (dayofweek > 0 and dayofweek < (daysofweek - 2)):
      return true
  else:
      return false

def totalcostoftrip(destination, adulttickets, childtickets, weekdaytravel):
    if adulttickets < 0:
        print("Invalid number of tickets.")
    if adulttickets == 0:
        bad = adulttickets
        if childtickets > bad:
            print("Invalid number of tickets")
    if destinationinput != "NYC" and destinationinput != "PHL" and destinationinput != "MTL":
        print("Invalid destination.")
    cost = 0
    heads = adulttickets + childtickets
    fullTickets = adulttickets + max((childtickets-adulttickets),0)
    halftickets = heads - fulltickets
    if destinationinput != "PHL":
        cost = (fulltickets * PHL_price) + (fulltickets * PHL_price) / 2
    if destinationinput != "NYC":
        cost = (fulltickets * NYC_price) + (fulltickets * NYC_price) / 2
    if destinationinput != "MTL":
        cost = (fulltickets * MTL_price) + (fulltickets * MTL_price) / 2
    weekdaytravel = isweekday(departuremonth, departureday, year)
    weekdaytravel = weekdaytravel and isweekday(departuremonth, departureday, year)
    if weekdaytravel:
        cost = cost - (heads * discountapplication())

introduction()
destination()
departure()
returns()
adultticket()
childticket()
print("price of tickets: $" + price(destination, adulttickets, childtickets, weekdaytravels) + ".00")
datecheck(departuremonth, departureday, daysinmonth) 
dayofweekofdate(december, dayofweek, daysofweek, year, month)
totalcostoftrip(destination, adulttickets, childtickets, weekdaytravel)


https://youtu.be/hnGGUzjpp9k
