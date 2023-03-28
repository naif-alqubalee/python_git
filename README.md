# python_git
the first project for me
import datetime # for import time
date = datetime.date.today()
customer_name = input("Enter customer name: ") # coustomer name
count = 0 # counter for seq
total = 0 
item_list = []
while True:
    item_name = input("enter type or press exit to close: ") 
    if item_name == "exit":
        break
    item_qty = int(input("enter item quantity: "))
    item_price = float(input("enter item price: "))
    item_amount = item_qty * item_price
    count += 1
    item_list.append([count, item_name, item_qty, item_price, item_amount ])
    total += item_amount
    discount = 0
    if total >= 1000:
        discount = total * 0.1
        total -= discount
print(f"Supermarket\n Date: {date}\n Customer Name: {customer_name}\n"
     f"seq |    item      |     qty     |     Until price     |    amount ")
for item in item_list:
    print(item[0],'      ', item[1] ,'          ', item[2],'          ',item[3],'          ', item[4] )
    print("")
print(f"total:{total}\n Discount:{discount}\n New Total:{total - discount}")
