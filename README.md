class vehicle:
    def __init__(self,name,mileage,capacity):
        self.name = name
        self.mileage = mileage
        self.capacity = capacity

    def fare(self):
        return self.capacity*100


class bus(vehicle):
    def fare(self):
        amt = super().fare()
        amt += amt*10/100
        return amt

obj1 = bus('volvo',10,50)
obj2 = vehicle("BMW",60,5)
print("total bus fare is :-",obj1.fare())
print("total vehicle fare is :-",obj2.fare()) 
