class dmart:
    def __init__(self):
      self.items = []
      
    def add_item (self, item_name, qty):
            item=(item_name, qty)
            self.items.append(item)

            
    def remove_item(self,item_name):
        for item in self.items:
            if item[0]== item_name:
                self.items.remove(item)
                break

                    
    def calculate_total (self):
        total = 0
        for item in self.items:
            total += item[1]
        return total
            
d = dmart ()
d.add_item("Mango", 369)
d.add_item("Fish",259)
d.add_item("Biscuit packet",159)

print ("Current Items in Cart:")
for item in d.items:
    print (item[0], "=", item[1])

total_qty = d.calculate_total()
print("Total Quantity:", total_qty)

d.remove_item("Mango")
print("\nupdated Items in Cart after removing Mango:")
for item in d.items:
    print(item[0],"_",item[1])
total_qty = d.calculate_total()
print("Total Quantity:",total_qty)
