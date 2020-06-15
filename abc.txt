class Transaction:
    def __init__(self,cust_name,accnt_balance):
        self.cust_name=cust_name
        self.accnt_balance=accnt_balance 
    def cust_info(self):
        print("Welcome to PayaPal ")
        print("Hi",self.cust_name)
        print("Your Total Balance in the account : ",self.accnt_balance)
    def usage_limit(self):
        if self.accnt_balance>=7000:
            print("Congratulations!")
            print("You got MakeMyTrip Cupon Offer!") 
        elif self.accnt_balance>=5000:
            print("Congratulations!")
            print("You Got BookMyShow Ticket Offer!") 
        elif self.accnt_balance>=3500:
            print("Congratulation!")
            print("You got 27 credit points!") 
        else:
            print("Sorry!,You are not qulaified for any offer.") 
Customers=int(input("Enter the Number of Customers!"))
for i in range(Customers):
    cust_name=input("Enter the Customer Name :") 
    accnt_balance=int(input("Enter the Balance Amount: ")) 
    info=Transaction(cust_name,accnt_balance) 
    info.cust_info()
    info.usage_limit() 
    print()

