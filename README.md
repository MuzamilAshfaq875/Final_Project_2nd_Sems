# Final_Project_2nd_Sems
class Category:
    def __init__(self, name, price, category):
        self.name = name
        self.price = price
        self.category = category

    def display_info(self):
        print("Name:", self.name)
        print("Price:", self.price)
        print("Category:", self.category)


class Electronics(Category):
    def __init__(self, name, price, brand):
        super().__init__(name, price, "Electronics")
        self.brand = brand

    def display_info(self):
        super().display_info()
        print("Brand:", self.brand)


class Book(Category):
    def __init__(self, name, price, author):
        super().__init__(name, price, "Book")
        self.author = author

    def display_info(self):
        super().display_info()
        print("Author:", self.author)


class Food(Category):
    def __init__(self, name, price, expiration_date):
        super().__init__(name, price, "Food")
        self.expiration_date = expiration_date

    def display_info(self):
        super().display_info()
        print("Expiration Date:", self.expiration_date)


class Shoes(Category):
    def __init__(self, name, price, size):
        super().__init__(name, price, "Shoes")
        self.size = size

    def display_info(self):
        super().display_info()
        print("Size:", self.size)


def add_product():
    category_choice = int(input("Select a category:\n1. Electronics\n2. Book\n3. Food\n4. Shoes\nEnter your choice: "))
    name = input("Enter the product name: ")
    price = float(input("Enter the product price: "))

    if category_choice == 1:
        brand = input("Enter the brand: ")
        product = Electronics(name, price, brand)
    elif category_choice == 2:
        author = input("Enter the author: ")
        product = Book(name, price, author)
    elif category_choice == 3:
        expiration_date = input("Enter the expiration date: ")
        product = Food(name, price, expiration_date)
    elif category_choice == 4:
        size = input("Enter the size: ")
        product = Shoes(name, price, size)
    else:
        print("Invalid category choice.")
        return

    print("Product added successfully.")
    return product


def remove_product(products):
    name = input("Enter the name of the product to remove: ")
    for product in products:
        if product.name == name:
            products.remove(product)
            print("Product removed successfully.")
            return
    print("Product not found.")


def display_products(products):
    if not products:
        print("No products available.")
    else:
        print("Products:")
        for product in products:
            product.display_info()
            print()


def main():
    products = []

    while True:
        print("\nMain Menu:")
        print("1. Add Product")
        print("2. Remove Product")
        print("3. Display Products")
        print("4. Exit")

        choice = int(input("Enter your choice (1-4): "))

        if choice == 1:
            product = add_product()
            if product:
                products.append(product)
        elif choice == 2:
            remove_product(products)
        elif choice == 3:
            display_products(products)
        elif choice == 4:
            print("Thank you for using the online shopping system!")
            break
        else:
            print("Invalid choice. Please enter a number from 1 to 4.")


if __name__ == "__main__":
    main()


class Category:
    def __init__(self, name, price, category):
        self.name = name
        self.price = price
        self.category = category

    def display_info(self):
        print("Name:", self.name)
        print("Price:", self.price)
        print("Category:", self.category)


class Electronics(Category):
    def __init__(self, name, price, brand):
        super().__init__(name, price, "Electronics")
        self.brand = brand

    def display_info(self):
        super().display_info()
        print("Brand:", self.brand)


class Book(Category):
    def __init__(self, name, price, author):
        super().__init__(name, price, "Book")
        self.author = author

    def display_info(self):
        super().display_info()
        print("Author:", self.author)


class Food(Category):
    def __init__(self, name, price, expiration_date):
        super().__init__(name, price, "Food")
        self.expiration_date = expiration_date

    def display_info(self):
        super().display_info()
        print("Expiration Date:", self.expiration_date)


class Shoes(Category):
    def __init__(self, name, price, size):
        super().__init__(name, price, "Shoes")
        self.size = size

    def display_info(self):
        super().display_info()
        print("Size:", self.size)


def main():
    # Create objects of different categories
    electronics = Electronics("TV", 999.99, "Samsung")
    book = Book("Python Crash Course", 29.99, "Eric Matthes")
    food = Food("Bread", 2.99, "2023-05-30")
    shoes = Shoes("Sneakers", 49.99, 9.5)

    # Display information of each object
    electronics.display_info()
    print()
    book.display_info()
    print()
    food.display_info()
    print()
    shoes.display_info()


if __name__ == "__main__":
    main()
 final project
