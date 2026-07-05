products = {
    1: {"name": "Black T-Shirt", "price": 599},
    2: {"name": "White Oversized Tee", "price": 799},
    3: {"name": "Printed Hoodie", "price": 1499}
}

cart = []

while True:
    print("\n=== APPAREL STORE ===")

    for pid, product in products.items():
        print(f"{pid}. {product['name']} - ₹{product['price']}")

    print("0. Exit")

    choice = int(input("\nSelect Product: "))

    if choice == 0:
        break

    if choice in products:
        cart.append(products[choice])
        print(f"{products[choice]['name']} added to cart!")

print("\n=== CART ===")
total = 0

for item in cart:
    print(f"{item['name']} - ₹{item['price']}")
    total += item['price']

print(f"\nTotal: ₹{total}")
print("Thank you for shopping!")
