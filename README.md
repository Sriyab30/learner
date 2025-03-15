# python_restaurant
menu ={ 
    'Pizza' :40,
    'pasta' :50,
    'burger':40,
    'Salad' :20,
    'coffee':80,
    'Python' :0.2,

}
print(menu)

print("welcome to python restaurant")
print("pizza: Rs40\nPasta: Rs50\nburger: Rs40\nSalad: Rs20\ncoffee: Rs80")

order_total = 0
order1 = input("Enter the name of the dish you want to order = ")
print("Your bill is: ", menu[order1])
order2 = input("Do you want to order more? : ")
if(order1 != "Coffee" and order2 == "No"):
    print("Your total bill is ", menu[order1] )
    
elif(order1 == "coffee" and order2 == "No"):
    print("Sorry sir, You Cant order just a coffee")
    print("Thank You")

else:
    total_bill = menu[order1]+menu[order2]
    coupon = (input("Do you have a coupon Code, if yes then enter it? :"))
    if(coupon == "Python"):
        disc_value = total_bill * menu[coupon]
        print("Your bill after 20% Discount: ", total_bill - disc_value)
    else:
        print("Your total bill is: ", menu[order1]+menu[order2])
    
print("Thank you for ordering")

