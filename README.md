totalflights=int()
tincome=int()
ptype=""
p1=str()
p2=str()
p3=str()
fp1=int()
fp2=int()
fp3=int()
t1=int()
t2=int()
t3=int()
print("First part is for the prediction")
flength=int(input("please enter your flight length 30 min or 60 min"))
totalflights=int(600/(flength+30))

print("Please enter the Plane type:")
print("p1 for 2seater", "p2 for 4seater", "p3 for historic plane", sep="\n")
ptype=str(input())
if ptype=='p1' and flength==30:
    tincome=tincome+(totalflights*100)
       
elif ptype=='p1' and flength==60:
    tincome=tincome+(totalflights*150)
         
elif ptype=='p2' and flength==30:
    tincome=tincome+(totalflights*120)
         
elif ptype=='p2' and flength==60:
    tincome=tincome+(totalflights*200)
         
elif ptype=='p3' and flength==30:
    tincome=tincome+(totalflights*300)
         
elif ptype=='p3' and flength==60:
    tincome=tincome+(totalflights*500)
         
print("total Projected income:", tincome)

#inputting flight time with respect to plane

p1tday=int(input("is 2 seater plane today running for 30 or 60 minutes?"))

p2tday=int(input("is 4 seater plane today running for 30 or 60 minutes?"))

p3tday=int(input("is historic plane today running for 30 or 60 minutes?"))

tp1=600

tp2=600

tp3=600

#setting minimum criteria for flight time

while (tp1>30)or(tp2>30)or(tp3>30):
   
	 ptype=input("Plane Type:")
    
		flength=int(input("enter time for flight"))
    
		if ptype=='p1' and flength==p1tday and tp1>(p1tday+30):
        
				print("booking success")
        
				tp1=tp1-p1tday
        
				fp1=fp1+1
        
				if p1tday==30:
             
						 t1=t1+100
        
				elif p1tday==60:
             
						 t1=t1+150
    
		elif ptype=='p2' and flength==p2tday and tp2>(p2tday+30):
        
				print("booking success")
        
				tp2=tp2-p2tday
        
				fp2=fp2+1
        
				if p2tday==30:
             
						 t2=t2+120
        
				elif p2tday==60:
             
						 t2=t2+200     
    
		elif ptype=='p3' and flength==p3tday and tp3>(p3tday+30):
        
				print("booking success")
        
				tp3=tp3-p3tday
        
				fp3=fp3+1
        
				if p3tday==30:
             
						 t3=t3+300
        
				elif p3tday==60:
             
						 t3=t3+500     
    
		else: print("error! Flight not Available")

gtotal=int(t1+t2+t3)

print("Total earnings for 2 seater plane:", t1)

print("Total flights for 2 seater plane:", fp1)

print("Total earnings for 4 seater plane:", t2)

print("Total flights for 4 seater plane:", fp2)

print("Total earnings for historic plane:", t3)

print("Total flights for historic plane:", fp3)

print("Total Earnings for the day:", gtotal)

print("Total number of flights for the day:",(fp1+fp2+fp3))             

