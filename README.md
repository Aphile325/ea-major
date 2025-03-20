from forex_python.converter import CurrencyRates

def ea_major():
    currency_rates = CurrencyRates()
    
    print("Welcome to EA Major - Your Ultimate Converter App!")
    print("Choose two currencies to convert between (e.g., USD to EUR):")
    
    from_currency = input("Enter the base currency code (e.g., USD): ").upper()
    to_currency = input("Enter the target currency code (e.g., EUR): ").upper()
    amount = float(input(f"Enter the amount in {from_currency}: "))
    
    try:
        converted_amount = currency_rates.convert(from_currency, to_currency, amount)
        print(f"{amount} {from_currency} is equivalent to {converted_amount:.2f} {to_currency}.")
    except Exception as e:
        print(f"Error: {e}")
        
if __name__ == "__main__":
    ea_major()
