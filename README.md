# class-variable
class Stationery_shop:
    bag=5
    no_of_cust = 15
    def __init__(self,customer_name,pen,pencil,chart,note,A4sheet):
        self.customer_name = customer_name
        self.pen = pen
        self.pencil = pencil
        self.chart = chart
        self.note = note
        self.A4sheet = A4sheet
        Stationery_shop.no_of_cust = Stationery_shop.no_of_cust+1
        
    def items(self):
        list = f"customer_name : {self.customer_name}\npen : {self.pen}\npencil : {self.pencil}\nchart : {self.chart}\nnote : {self.note}\nA4sheet : {self.A4sheet}"
        return list
    
    def pay_bag(self,amount):
        self.bag = self.bag + amount
        
cust1 = Stationery_shop('nivi',5,10,30,40,200)
cust2 = Stationery_shop('hari',15,20,40,45,250)

cust1.pay_bag(285)
cust2.pay_bag(370)

print(cust1.bag)
print(cust2.bag)
print(Stationery_shop.no_of_cust)
