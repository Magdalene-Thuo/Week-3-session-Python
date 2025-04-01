# Week-3-session-Python
----
def calculate_discount(price, discount_percent):
    """
    Calculate the final price after applying a discount.
    If the discount percentage is 20% or higher, apply the discount.
    Otherwise, return the original price.
    
    :param price: float, original price of the item
    :param discount_percent: float, discount percentage
    :return: float, final price after applying discount
    """
    if discount_percent >= 20:
        discount_amount = (discount_percent / 100) * price
        return price - discount_amount
    else:
        return price

# Prompt user for input
try:
    original_price = float(input("Enter the original price of the item: "))
    discount_percentage = float(input("Enter the discount percentage: "))
    
    # Calculate final price
    final_price = calculate_discount(original_price, discount_percentage)
    
    # Print result
    print(f"Final price after discount: {final_price:.2f}")
except ValueError:
    print("Please enter valid numerical values for price and discount percentage.")
