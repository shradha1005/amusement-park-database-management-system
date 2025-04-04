# amusement-park-database-management-system
# amusement-park-database-management-system
import mysql.connector as sqltor 
con=sqltor.connect(host="localhost",user="root",password="devi",d
 atabase="Amusement_Park") 
if con.is_connected(): 
        print("Connected with mysql database successfully") 
else: 
         print("Connection Error. Please try again.") 
cursor=con.cursor() 
 
def createtables(): 
        ch="y" 
        while ch.lower()=="y": 
                print("Choose the table to be created from the menu") 
                print("1.Customers") 
                print("2.Water_Games") 
                print("3.Land_Games") 
                x=int(input("Enter your choice")) 
                if x==1: 
                        query="Create table if not exists customers(sno integer 
not null primary key ,custid char(4), custname 
varchar(30),custgender varchar(10),custage integer, game_category 
varchar(20), gameid1 char(4))" 
                        cursor.execute(query) 
                if x==2: 
 
                        query="Create table if not exists Water_Games(gameid 
char(4) not null primary key,gamename varchar(20),game_category 
varchar(20), min_age integer, entryfees integer)" 
                        cursor.execute(query) 
                if x==3: 
                        query="Create table if not exists Land_Games(gameid 
char(4) not null primary key,gamename varchar(20),game_category 
varchar(20), min_age integer , entryfees integer)" 
                        cursor.execute(query) 
                print("Table",x,"created")        
                ch=input("Do you want to create another table?(y /n)") 
 
 
def insertcust(): 
         ch="y" 
         while ch.lower()=="y": 
                  sno=int(input("Enter the serial number")) 
                  custid=input("Enter customer ID") 
                  custname=input("Enter customer's name") 
                  custgender=input("Enter customer's gender") 
                  custage=int(input("Enter customer's age ")) 
                  gamecat=input("Enter the category of game 
chosen(LG/WG)") 
                  gameid=input("Enter game ID") 
                  query="insert into 
customers(sno,custid,custname,custgender,custage,game_category, 
gameid1) 
values({},'{}','{}','{}',{},'{}','{}')".format(sno,custid,custname,custgender
 ,custage,gamecat,gameid) 
                  cursor.execute(query) 
                  con.commit() 
                  ch=input("Do you want to enter another record?(y/n)") 
 
 
def insertwgame(): 
 
         query1="insert into 
Water_Games(gameid,gamename,game_category,min_age,entryfee
 s)values('{}','{}','{}',{},{})".format("WG01","Water 
Wars","WG",10,1200) 
         cursor.execute(query1) 
         con.commit() 
         query2="insert into 
Water_Games(gameid,gamename,game_category,min_age,entryfee
 s)values('{}','{}','{}',{},{})".format("WG02","Water 
volcano","WG",10,1200) 
         cursor.execute(query2) 
         con.commit() 
         query3="insert into 
Water_Games(gameid,gamename,game_category,min_age,entryfee
 s)values('{}','{}','{}',{},{})".format("WG03","Boating","WG",12,1500) 
         cursor.execute(query3) 
         con.commit() 
         query4="insert into 
Water_Games(gameid,gamename,game_category,min_age,entryfee
 s)values('{}','{}','{}',{},{})".format("WG04","Frog slide","WG",10,1000) 
         cursor.execute(query4) 
         con.commit() 
         query5="insert into 
Water_Games(gameid,gamename,game_category,min_age,entryfee
 s)values('{}','{}','{}',{},{})".format("WG05","Rain dance","WG",6,800) 
         cursor.execute(query5) 
         con.commit() 
         query6="insert into 
Water_Games(gameid,gamename,game_category,min_age,entryfee
 s)values('{}','{}','{}',{},{})".format("WG06","Tornado 
Coaster","WG",10,1200) 
         cursor.execute(query6) 
         con.commit() 
         query7="insert into 
Water_Games(gameid,gamename,game_category,min_age,entryfees)values('{}','{}','{}',{},{})".format("WG07","3 Lane 
slides","WG",10,1200) 
         cursor.execute(query7) 
         con.commit() 
         query8="insert into 
Water_Games(gameid,gamename,game_category,min_age,entryfee
 s)values('{}','{}','{}',{},{})".format("WG08","Swimming 
pool","WG",6,1000) 
         cursor.execute(query8) 
         con.commit() 
         query9="insert into 
Water_Games(gameid,gamename,game_category,min_age,entryfee
 s)values('{}','{}','{}',{},{})".format("WG09","Dome 
slide","WG",10,1200) 
         cursor.execute(query9) 
         con.commit() 
         query10="insert into 
Water_Games(gameid,gamename,game_category,min_age,entryfee
 s)values('{}','{}','{}',{},{})".format("WG10","aqua race","WG",10,1200) 
         cursor.execute(query10) 
         con.commit() 
          
 
 
def insertlgame(): 
         query1="insert into 
Land_Games(gameid,gamename,game_category,min_age,entryfees)
 values('{}','{}','{}',{},{})".format("LG01","Roller Coaster","LG",9,1300) 
         cursor.execute(query1) 
         con.commit() 
         query2="insert into 
Land_Games(gameid,gamename,game_category,min_age,entryfees)
 values('{}','{}','{}',{},{})".format("LG02","Ferris Wheel","LG",12,1500) 
         cursor.execute(query2) 
         con.commit()  
         query3="insert into 
Land_Games(gameid,gamename,game_category,min_age,entryfees)
 values('{}','{}','{}',{},{})".format("LG03","Haunted 
house","LG",13,1000) 
         cursor.execute(query3) 
         con.commit() 
         query4="insert into 
Land_Games(gameid,gamename,game_category,min_age,entryfees)
 values('{}','{}','{}',{},{})".format("LG04","Flat rides","LG",10,1200) 
         cursor.execute(query4) 
         con.commit() 
         query5="insert into 
Land_Games(gameid,gamename,game_category,min_age,entryfees)
 values('{}','{}','{}',{},{})".format("LG05","Bumper cars","LG",8,800) 
         cursor.execute(query5) 
         con.commit() 
         query6="insert into 
Land_Games(gameid,gamename,game_category,min_age,entryfees)
 values('{}','{}','{}',{},{})".format("LG06","Sonic colours","LG",5,1000) 
         cursor.execute(query6) 
         con.commit() 
         query7="insert into 
Land_Games(gameid,gamename,game_category,min_age,entryfees)
 values('{}','{}','{}',{},{})".format("LG07","Merry Go Road","LG",8,1000) 
         cursor.execute(query7) 
         con.commit() 
         query8="insert into 
Land_Games(gameid,gamename,game_category,min_age,entryfees)
 values('{}','{}','{}',{},{})".format("LG08","Free fall","LG",12,1500) 
         cursor.execute(query8) 
         con.commit() 
         query9="insert into 
Land_Games(gameid,gamename,game_category,min_age,entryfees)
 values('{}','{}','{}',{},{})".format("LG09","Haunted train","LG",10,1200) 
         cursor.execute(query9)  
         con.commit() 
         query10="insert into 
Land_Games(gameid,gamename,game_category,min_age,entryfees)
 values('{}','{}','{}',{},{})".format("LG10","Shoot and win","LG",9,1000) 
         cursor.execute(query10) 
         con.commit() 
                   
 
 
def display_customers(): 
    query="select * from customers" 
    cursor.execute(query) 
    x=cursor.fetchall() 
    for i in x: 
        print("Entry number:",i[0])      
        print("Customer ID:",i[1]) 
        print("Customer name:",i[2]) 
        print("Customer gender:",i[3]) 
        print("Customer age:",i[4]) 
        print("Game category:",i[5]) 
        print("Game ID:",i[6]) 
        print() 
 
def display_Watergames(): 
    query="select * from Water_Games" 
    cursor.execute(query) 
    x=cursor.fetchall() 
    for i in x: 
        print("Game ID:",i[0]) 
        print("Game name:",i[1]) 
        print("Game category:",i[2]) 
        print("Minimum age:",i[3]) 
        print("Entry fees:",i[4]) 
        print() 

 
def display_Landgames(): 
    query="select * from Land_Games" 
    cursor.execute(query) 
    x=cursor.fetchall() 
    for i in x: 
        print("Game ID",i[0]) 
        print("Game name:",i[1]) 
        print("Game category:",i[2]) 
        print("Minimum age:",i[3]) 
        print("Entry fees:",i[4]) 
        print() 
 
def join_tables(): 
    print("Choose the tables that you'd like to join from the menu") 
    print("1.Customers and Water_Games") 
    print("2.Customers and Land_Games") 
    x=int(input("Enter your choice")) 
    if x==1: 
        query="select custid,custname, gameid,gamename from 
Customers,Water_Games where 
customers.gameid1=Water_Games.gameid and 
Customers.custage>=Water_Games.min_age"                    
        cursor.execute(query) 
        x=cursor.fetchall() 
        for i in x: 
            print(i) 
    if x==2: 
        query="select custid,custname,gameid,gamename from 
Customers,Land_Games where 
customers.gameid1=Land_Games.gameid and 
Customers.custage>=Land_Games.min_age" 
        cursor.execute(query) 
        x=cursor.fetchall() 
        for i in x: 
            print(i) 
 
 
def bill(): 
        ch="y" 
        while ch.lower()=="y": 
                x=input("Enter the customer's ID whose bill is to be 
prepared") 
                y=input("Enter the Customer's name") 
                query1="select custname,gamename,entryfees from 
customers, Land_Games where 
customers.gameid1=Land_Games.gameid and custid='{}'".format(x) 
                cursor.execute(query1) 
                a=cursor.fetchall() 
                query2="select custname,gamename,entryfees from 
customers, Water_Games where 
customers.gameid1=Water_Games.gameid and custid='{}'".format(x) 
                cursor.execute(query2) 
                b=cursor.fetchall() 
                print("﹌﹌﹌﹌﹌﹌﹌﹌﹌MAGIC KINGDOM PARK﹌﹌﹌
 ﹌﹌﹌﹌﹌﹌") 
                print("Name:",y) 
                s1=0 
                s2=0 
                for i in a: 
                    print("Entryfees of the game",i[1],": ₹",i[2]) 
                    lsum=s1+i[2] 
                    s1=lsum    
                for j in b: 
                    print("Entryfees of the game",j[1],": ₹",j[2]) 
                    wsum=s2+j[2] 
                    s2=wsum 
                total=lsum +wsum 
                gst=total*0.18 
                print("Actual price: ₹",total) 
                print("GST amount: ₹",gst) 
                print("Total amount : ₹",total+gst) 
                print() 
                print("Thank you for coming!") 
                print("Have a great day!") 
                print() 
                print("✩｡:*•.────────  ❁ ❁ ────────.•*:｡✩") 
                print() 
                print() 
                ch=input("Do you want to get the bill for another 
customer?(y/n)") 
                 
def delete_tables(): 
         ch="y" 
         while ch.lower()=="y": 
                  print("Choose the table that you'd like to delete from the 
menu :") 
                  print("1.Customers") 
                  print("2.Water_Games") 
                  print("3.Land_Games") 
                  x=int(input("Enter your choice")) 
                  if x==1: 
                           cursor.execute("drop table if exists Customers") 
                           con.commit() 
                  if x==2: 
                           cursor.execute("drop table if exists Water_Games") 
                           con.commit() 
                  if x==3: 
                           cursor.execute("drop table if exists Land_Games") 
                           con.commit() 
                  print("Table ",x,"deleted")         
                  ch=input("Do you want to delete another table?(y/n)")          
 
z="y" 
while z.lower()=="y": 
    print("Choose the task to be done from the menu:") 
    print("1.To Create the required tables (Customers, Water_Games, 
Land_Games)") 
    print("2.To insert records into the table 'Customers' ") 
    print("3.To insert records into the table 'Water_Games' ") 
    print("4.To insert records into the table 'Land_Games' ") 
    print("5.To display the records in the table 'Customers' ") 
    print("6.To display the records in the table 'Water_Games' ") 
    print("7.To display the records in the tabe 'Land_Games' ") 
    print("8.To join two tables and display the content") 
    print("9.To issue the bill for the customer") 
    print("10.To delete a table from the database") 
    c=int(input("Enter your choice")) 
    if c==1: 
        createtables() 
    if c==2: 
        insertcust() 
    if c==3: 
        insertwgame() 
    if c==4: 
        insertlgame() 
    if c==5: 
        display_customers() 
    if c==6: 
        display_Watergames() 
    if c==7: 
        display_Landgames() 
    if c==8: 
        join_tables() 
    if c==9: 
        bill()      
    if c==10: 
        delete_tables() 
    print()    
 z=input("Do you want to do another task?(y/n)"  
con.close()    
