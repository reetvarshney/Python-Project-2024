import random

# Global variables
b_amount = 0
s_amount = 0
occupied_seats = 0
no = 0 

# Welcome message
print("                              WELCOME TO CHALCHITRA CINEMAS")
print("                                  Entertainment Downtown")


# Function to display menu options
def welcome():
    print("\n 1. Type 1 to book movie Tickets")
    print("\n 2. Type 2 to orders Snacks")
    print("\n 3. Type 3 to order Beverages")
    print("\n 4. Type 4 to Exit")


# Function to book movie tickets
def book_ticket():
    global occupied_seats
    print("Movies currently screening\n")

    # Dictionary containing movie options
    movies = {
        1: "Dil Chahta Hai",
        2: "Jab We Met",
        3: "Drishyam"
    }

    # Displaying movie options
    for key, value in movies.items():
        print(f"{key}. {value}")

    m = int(input("Enter your desired Movie (option): "))  # Getting user input for movie choice
    global mov

    if m in movies:
        mov = movies[m]
    else:
        print("Input Invalid")
        book_ticket()
    
    update_seat_count()  # Update seat count after booking


# Function to update seat count
def update_seat_count():
    global occupied_seats
    occupied_seats += no  # Increment the number of occupied seats


# Function to select number of movie tickets
def no_of_tickets():
    global no, seats
    print("Selection of Seats:-")
    no = int(input("\nNumber of tickets you want to book (max. limit=50): "))  # Getting user input for number of tickets

    if no == 1:
        print("Type'1' to select a seat at random OR '2' to select them yourself")
        c = int(input("Enter choice: "))
        if c == 1:
            seats = random.randint(1, 50)  # Generating random seat number
            print("The seat allotted is: ", seats)
        elif c == 2:
            seats = int(input("Enter the seat no. you would like to select (b/w 1 to 50): "))  # Getting user input for seat number
            print("The seat allotted is: ", seats)
        else:
            print("Input Invalid")
    elif 1 < no <= 50:
        seats = []
        print("Type '1' for the seats to be selected for you OR '2' to select them yourself ")
        c = int(input("Enter choice: "))
        if c == 1:
            seat = random.randint(1, 50)  # Generating random seat number
            for _ in range(no):
                seats.append(seat)
                seat += 1
            print("The seat allotted is: ", seats)
        elif c == 2:
            for _ in range(no):
                seat = int(input("Enter the seat no. you would like to select (b/w 1 to 50): "))  # Getting user input for seat number
                seats.append(seat)
            print("The seats allotted is: ", seats)
        else:
            print("Input Invalid")
    else:
        print("Input Invalid")
        no_of_tickets()

    global bno
    bno = random.randint(1000, 10000)  # Generating random booking number

# Function to select movie day
def movie_day():
    print("\nSelection of Day:-")
    days = {
        1: {"Day": "Thu", "Date": "2024-04-25", "Time1": 1200, "Time2": 1400, "Time3": 1800},
        2: {"Day": "Fri", "Date": "2024-04-26", "Time1": 1200, "Time2": 1400, "Time3": 1800},
        3: {"Day": "Sat", "Date": "2024-04-27", "Time1": 1200, "Time2": 1400, "Time3": 1800},
        4: {"Day": "Sun", "Date": "2024-04-28", "Time1": 1200, "Time2": 1400, "Time3": 1800},
    }

    # Displaying day options
    for key, value in days.items():
        print(f"{key}. {value['Day']} - {value['Date']} - Times: {value['Time1']}, {value['Time2']}, {value['Time3']}")

    d = int(input("Enter the preferred Day (option): "))  # Getting user input for day selection

    global day, date

    if d in days:
        day = days[d]['Day']
        date = days[d]['Date']
    else:
        print("Input Invalid")
        movie_day()
   
# Function to select movie time
def movie_time():
    global time
    time = int(input("Enter your preferred Timings (Hrs): "))  # Getting user input for time selection

# Function to enter customer details
def ent_details():
    global name, age, mob_no
    print("\nEnter your Personal Details:-")
    name = input("Your Name: ")
    age = int(input("Your Age: "))
    mob_no = int(input("Your Contact number: "))


# Function to calculate and display movie payment details
def movie_payment():
    global m_amount
    print("Bill For Movie:")
    m_amount = no * 450  # Calculating total movie ticket amount based on number of tickets
    print("Payable amount for movie tickets= Rs ", m_amount)


# Function to process total payment for movie tickets
def total_payment_movie():
    print("Movie Bill:-")
    print("Total amount= Rs ", m_amount)
    payment = int(input("Pay total amount: Rs "))  # Getting user input for payment amount
    if payment == m_amount:
        OTP = int(input("Enter the OTP (default-123456): "))  # Getting user input for OTP
        if OTP == 123456:
            print("PAYMENT FOR MOVIE TICKET CONFIRMED")
        else:
            print("ERROR IN PAYMENT")
            print("\n")
            total_payment_movie()
    else:
        print("ERROR IN PAYMENT")
        print("\n")
        total_payment_movie()


# Function to generate and display movie receipt
def movie_receipt():
    print("                              CHALCHITRA CINEMAS\n")
    print("                                  Name:\t", name)
    print("                Price of single ticket:\t", "Rs 450")
    print("              No. of tickets purchased:\t", no)
    print("         Total amount of movie tickets:\t", "Rs", m_amount, '\n')
    print("                         Thank You For Choosing Us!\n")


# Function to generate and display movie ticket
def movie_ticket():
    global ticket_no
    ticket_no = random.randint(1000, 9999)  # Generating random ticket number
    print("                             CHALCHITRA CINEMAS\n")
    print("                        Movie selected:\t", mov)
    print("                                   Day:\t", day)
    print("                                  Time:\t", time, "Hrs" )
    print("                           Seat number(s):\t", seats, '\n')
    print("\t                               ENJOY!!\n")


# Function to book snacks
def book_snacks():
    global snacks, snack_no, s_amount
    print("MENU")
    print("Snacks\n")

    # List of available snacks with their prices
    snacks_table = [
        {"SNo": 1, "Snacks": "Cheesy Nachos", "Price": 150.00},
        {"SNo": 2, "Snacks": "Butter Popcorn", "Price": 200.00},
        {"SNo": 3, "Snacks": "Veg Cheese Burger", "Price": 250.00},
        {"SNo": 4, "Snacks": "Cheesy Toast", "Price": 250.00},
        {"SNo": 5, "Snacks": "Veg Fried Momos", "Price": 200.00}
    ]

    # Displaying snack options
    for item in snacks_table:
       if 'Price' in item:
           print(f"{item['SNo']}. {item['Snacks']} - Rs{item['Price']:.2f}")
       else:
           print(f"{item['SNo']}. {item['Snacks']} - Price not available")

    snack_no = int(input("\nEnter the number of snacks to be purchased (max. limit=5): "))  # Getting user input for number of snacks

    if snack_no <= 5:
        count = 1
        while count <= snack_no:
            s1 = int(input("Enter the Snack to be ordered (option): "))  # Getting user input for snack choice
            if 1 <= s1 <= 5:
                s_amount += snacks_table[s1 - 1]["Price"]  # Adding snack price to total amount
            else:
                print("Input Invalid")
                continue
            count += 1
    else:
        print("Input Invalid")


# Function to calculate and display snack payment details
def snack_payment():
    global s_amount
    print("Bill For Snacks:")
    print("Payable amount for Snacks= Rs", s_amount)


# Function to generate and display snack receipt
def snacks_receipt():
    print("                          CHALCHITRA CINEMAS\n")
    print("                 Your Order For Snacks:\t", snacks)
    print("               No. of snacks purchased:\t", snack_no)
    print("               Total amount for snacks:\t", "Rs", s_amount, '\n')
    print("                     Thank You For Choosing Us!\n")


# Function to book beverages
def book_beverages():
    global bev_no, bev, b_amount
    print("MENU")
    print("Beverages\n")

    # List of available beverages with their prices
    beverages_table = [
        {"SNo": 1, "Drink": "Soft Drinks", "Price": 120.00},
        {"SNo": 2, "Drink": "Cold Coffee", "Price": 300.00},
        {"SNo": 3, "Drink": "Hot Coffee", "Price": 250.00},
        {"SNo": 4, "Drink": "Iced Tea", "Price": 200.00},
        {"SNo": 5, "Drink": "Blue Lagoon", "Price": 350.00}
    ]

    # Displaying beverage options
    for item in beverages_table:
        if 'Price' in item:
            print(f"{item['SNo']}. {item['Drink']} - Rs{item['Price']:.2f}")
        else:
            print(f"{item['SNo']}. {item['Drink']} - Price not available")
        

    bev_no = int(input("Enter the number of Beverages to be purchased (max. limit=5): "))  # Getting user input for number of beverages

    if bev_no <= 5:
        count = 1
        b_amount = 0
        while count <= bev_no:
            b1 = int(input("Enter the Beverage to be ordered (option): "))  # Getting user input for beverage choice
            if 1 <= b1 <= 5:
                b_amount += beverages_table[b1 - 1]["Price"]  # Adding beverage price to total amount
            else:
                print("Input Invalid")
                continue
            count += 1
    else:
        print("Input Invalid")


# Function to calculate and display beverage payment details
def beverages_payment():
    global b_amount
    print("Bill For Beverages:")
    print("Amount for beverages= Rs", b_amount)


# Function to generate and display beverage receipt
def beverages_receipt():
    print("                         CHALCHITRA CINEMAS\n")
    print("              Your Order For Beverages: \t", bev)
    print("            No. of Beverages purchased: \t", bev_no)
    print("            Total amount for Beverages: \t", "Rs", b_amount)
    print("            Total amount for Beverages: \t", b_amount, '\n')
    print("                     Thank You For Choosing Us!\n")


# Function to calculate total payment for snacks and beverages
def total_payment_food():
    global total_amount_food
    print("Final Bill For Snacks & Beverages: ")
    total_amount_food = s_amount + b_amount  # Calculating total amount for snacks and beverages
    print("Total payable amount for Food= Rs ", total_amount_food)
    payment = int(input("Pay total amount for Food: Rs "))
    if payment == total_amount_food:
        OTP = int(input("Enter the OTP (default- 123456): "))
        if OTP == 123456:
            print("PAYMENT FOR SNACKS & BEVERAGES CONFIRMED")
        else:
            print("ERROR IN PAYMENT")
            print("\n")
            total_payment_food()
    else:
        print("ERROR IN PAYMENT")
        print("\n")
        total_payment_food()


# Function to generate and display receipt for snacks and beverages
def food_receipt():
    print("                         CHALCHITRA CINEMAS\n")
    print("               No. of snacks purchased:\t", snack_no)
    print("               Total amount for Snacks:\t", "Rs", s_amount, '\n')
    print("            \n No. of Beverages purchased:\t", bev_no)
    print("            Total amount for Beverages:\t", "Rs", b_amount, '\n')
    print("   \n Total amount for Snacks & Beverages:\t", total_amount_food, '\n')
    print("                      Thank You For Choosing Us!\n")


# Function to process total payment for snacks
def total_payment_snacks():
    global s_amount
    print("Snacks Bill:")
    print("Total payable amount for snacks= Rs", s_amount)
    payment = int(input("Pay total amount for snacks: Rs "))
    if payment == s_amount:
        OTP = int(input("Enter the OTP (default- 123456): "))
        if OTP == 123456:
            print("PAYMENT FOR SNACKS CONFIRMED")
        else:
            print("ERROR IN PAYMENT")
            print("\n")
            total_payment_snacks()
    else:
        print("ERROR IN PAYMENT")
        print("\n")
        total_payment_snacks()


# Function to process total payment for beverages
def total_payment_beverages():
    global b_amount
    print("Beverages Bill:")
    print("Total amount for beverages= Rs", b_amount)
    payment = int(input("Pay total amount for beverages: Rs"))
    if payment == b_amount:
        OTP = int(input("Enter the OTP: "))
        if OTP == 123456:
            print("PAYMENT FOR BEVERAGES CONFIRMED")
        else:
            print("ERROR IN PAYMENT")
            print("\n")
            total_payment_beverages()
    else:
        print("ERROR IN PAYMENT")
        print("\n")
        total_payment_beverages()


# Function to display total receipt
def total_receipt():
    global t_amount
    t_amount = m_amount + b_amount + s_amount  # Calculating total amount
    print(f"Final Bill For Tickets, Snacks & Beverages: Rs{t_amount}")  # Displaying total amount
    print("THANK YOU!!!")
    print("Visit Again")


# Display menu options
welcome()

# Main loop for user interaction
while True:
    choice = int(input("\nEnter your choice: "))  # Getting user choice

    if choice == 1:  # Book ticket option
        ent_details()  # Enter customer details
        print("\nBOOK TICKET\n")
        book_ticket()  # Book movie ticket
        movie_day()  # Select movie day
        movie_time()  # Select movie time
        print(f"\nThank you! You have selected to watch {mov} on {day} at {time} HRS.\n")
        no_of_tickets()  # Select number of tickets
        print("\n")
        movie_payment()  # Calculate movie payment
        print("\n")
        total_payment_movie()  # Process total payment for movie
        print("\n")
        movie_receipt()  # Generate and display movie receipt
        print("\n")
        movie_ticket()  # Generate and display movie ticket
        print("\nDo you want to buy Snacks? (if yes click 'y' or if not click any alphabet key):")
        a = input("\nEnter choice: ").lower()  # Getting user choice for buying snacks
        if a == 'y':
            print("\n")
            book_snacks()  # Book snacks
            snack_payment()  # Calculate snack payment
            print("\nDo you want to buy Beverages? (if yes click 'y' or if not click any alphabet key):")
            b = input("\nEnter choice: ").lower()  # Getting user choice for buying beverages
            if b == 'y':
                print("\n")
                book_beverages()  # Book beverages
                beverages_payment()  # Calculate beverage payment
                print("\n")
                total_payment_food()  # Process total payment for food
                print("\n")
                food_receipt()  # Generate and display receipt for snacks and beverages
                print("\n")
            else:
                print("\n")
                total_payment_snacks()  # Process total payment for snacks only
                print("\n")
                snacks_receipt()  # Generate and display receipt for snacks
                print("\n")
        else:
            print("\n")
    elif choice == 2:  # Book snacks option
        print("BOOK SNACKS\n")
        book_snacks()  # Book snacks
        snack_payment()  # Calculate snack payment
        print("\nDo you want to buy Beverages? (if yes click 'y' or if not click any alphabet key):")
        b = input("\nEnter choice: ").lower()  # Getting user choice for buying beverages
        if b == 'y':
            print("\n")
            book_beverages()  # Book beverages
            beverages_payment()  # Calculate beverage payment
            print("\n")
            ent_details()  # Enter customer details
            print("\n")
            total_payment_food()  # Process total payment for food
            print("\n")
            food_receipt()  # Generate and display receipt for snacks and beverages
            print("\n")
        else:
            print("\n")
            ent_details()  # Enter customer details
            print("\n")
            total_payment_snacks()  # Process total payment for snacks only
            print("\n")
            snacks_receipt()  # Generate and display receipt for snacks
            print("\n")
    elif choice == 3:  # Book beverages option
        print("BOOK BEVERAGES\n")
        book_beverages()  # Book beverages
        beverages_payment()  # Calculate beverage payment
        print("\nDo you want to buy Snacks? (if yes click 'y' or if not click any alphabet key):")
        b = input("\nEnter choice: ").lower()  # Getting user choice for buying snacks
        if b == 'y':
            print("\n")
            book_snacks()  # Book snacks
            snack_payment()  # Calculate snack payment
            print("\n")
            ent_details()  # Enter customer details
            print("\n")
            total_payment_food()  # Process total payment for food
            print("\n")
            food_receipt()  # Generate and display receipt for snacks and beverages
            print("\n")
        else:
            print("\n")
            ent_details()  # Enter customer details
            print("\n")
            total_payment_beverages()  # Process total payment for beverages only
            print("\n")
            beverages_receipt()  # Generate and display receipt for beverages
            print("\n")
    elif choice == 4:  # Exit option
        print("THANK YOU!!!")
        break
    else:
        print("Input Invalid")
        print("\n")

# Display total receipt
total_receipt()
