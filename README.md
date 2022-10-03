# To-do-list-
user_input = (" choice")
data= [ ]

def show_menu():
    print ("""Menu:
    1. Add an item
    2. Mark as done
    3. View items 
    4. Exist """)


while user_input !=4 :
    show_menu()
    user_input = input(" Enter your choice :")

    if user_input=='1':
        item = input (" What is to be done?")
        data.append(item)
        print(" Added an item", item)
    elif user_input=='2':
        item = input(" What is to be marked as done ?")
        if item in data:
         data.remove(item)
         print(" Removed item:",item)
        else:print("  Item dose not exist in the list")

    elif user_input =='3':
        print(" The list od to-do items :")
        for item in data :
            print (item)
    elif not user_input != '4':
        print (" Goodbye")
    else :
        print (" Please enter one of 1,1 2, 3 or 4")
