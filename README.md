import Hotel as Hp

def main():
    print("----- Welcome to the Morgan La Casa -----\n")
    inp = input("Are you Manager or Customer(M/C): ")
    print("")
    if inp == "C":
        Hot = Hp.Hotel(200,3) 
        print(" The total number of rooms available are: " +str(Hot.get_totalspace()))
        print(" There are " + str(Hot.get_number_of_rooms()) + " rooms available across " + str(Hot.get_num_of_floors()) + " floors.")
        print("")
        print(" These are our room options: \n")
        print("-------------------\n")
        print(" The Regular room package")
        reg = Hp.basic("1 Air conditioning unit","1 Television unit","1 Regular Bathroom","1 Twin Bed")
        reg.set_num_of_rooms(100)
        reg.set_price(70)
        print("\n Bed: " + str(reg.get_number_of_bed()))
        print(" Air conditioning: " + str(reg.get_aircon()))
        print(" Television: " + str(reg.get_num_tv()))
        print(" Bathroom: " + str(reg.get_num_bathrooms()))
        print(" Price: $" + str(reg.get_price()) + " a night")
        print(" Number of rooms: There are a " + str(reg.get_num_of_rooms()) + " Regular Rooms each on the three floors\n")

        print("-------------------\n")
        print(" The Deluxe room package")
        dlx = Hp.deluxe("1 Air conditioning unit","1 Television unit","1 Regular Bathroom","1 Queen Sized Bed"," Service available")
        dlx.set_num_of_rooms(60)
        dlx.set_price(150)
        print("\n Bed: " + str(dlx.get_number_of_bed()))
        print(" Air Conditioning: " + str(reg.get_aircon()))
        print(" Television: " + str(dlx.get_num_tv()))
        print(" Bathroom: " + str(dlx.get_num_bathrooms()))
        print(" Room Service: " +str(dlx.get_room_service_coins()))
        print(" Price: $" + str(dlx.get_price()) + " a night")
        print(" Rooms: There are " + str(dlx.get_num_of_rooms()) + " Deluxe rooms on each of the three floors")

        print("\n-------------------\n")
        print(" The Premium room package")
        prm = Hp.baller("2 Air conditioning units","2 Television units","1 Premiuim Bathroom","2 Queen Sized Bed"," Service available", "Jacuzzi Available", "Snack Machine Available")
        prm.set_num_of_rooms(40)
        prm.set_price(300)
        print("\n Bed: " + str(prm.get_number_of_bed()))
        print(" Air Conditioning: " + str(prm.get_aircon()))
        print(" Television: " + str(prm.get_num_tv()))
        print(" Bathroom: " + str(prm.get_num_bathrooms()))
        print(" Room Service: " +str(prm.get_room_service_coins()))
        print(" Jacuzzi: " + str(prm.get_jaccuzi()))
        print(" Snack Machine: " + str(prm.get_snack_machine_coins()))
        print(" Price: $" + str(prm.get_price()) + " a night")
        print(" Rooms: There are " + str(prm.get_num_of_rooms()) + " Deluxe rooms on each of the three floors")
    
    elif inp == "M":
        print('Welcome Manager\n')
        csh = int(input("Input the amount of money earned this month: $") ) 
        Mth = input("Enter the current Month(J,F,M,A,MY,JU,JL,AU,S,O,N,D): ")
        print("")
        infile = open("business.txt","r")
        for line in infile:
            lst = line.split(",")
        print("-------------------\n")
        if Mth == "J":
            if csh < int(lst[0]):
                print("There is a reduce in profits compred to last year. $" + str((int(lst[0])-csh)) + " less")
            else:
                print("There is no Reduce of profits Compared to last year")
        if Mth == "F":
            if csh < int(lst[1]):
                print("There is a reduce in profits compred to last year. $" + str((int(lst[1])-csh)) + " less")
            else:
                print("There is no Reduce of profits Compared to last year")
        if Mth == "M":
            if csh < int(lst[2]):
                print("There is a reduce in profits compred to last year. $" + str((int(lst[2])-csh)) + " less")
            else:
                print("There is no Reduce of profits Compared to last year")
        if Mth == "A":
            if csh < int(lst[3]):
                print("There is a reduce in profits compred to last year. $" + str((int(lst[3])-csh)) + " less")
            else:
                print("There is no Reduce of profits Compared to last year")
        if Mth == "MY":
            if csh < int(lst[4]):
                print("There is a reduce in profits compred to last year. $" + str((int(lst[4])-csh)) + " less")
            else:
                print("There is no Reduce of profits Compared to last year")
        if Mth == "JU":
            if csh < int(lst[5]):
                print("There is a reduce in profits compred to last year. $" + str((int(lst[5])-csh)) + " less")
            else:
                print("There is no Reduce of profits Compared to last year")
        if Mth == "JL":
            if csh < int(lst[6]):
                print("There is a reduce in profits compred to last year. $" + str((int(lst[6])-csh)) + " less")
            else:
                print("There is no Reduce of profits Compared to last year")
        if Mth == "AU":
            if csh < int(lst[7]):
                print("There is a reduce in profits compred to last year. $" + str((int(lst[7])-csh)) + " less")
            else:
                print("There is no Reduce of profits Compared to last year")
        if Mth == "S":
            if csh < int(lst[8]):
                print("There is a reduce in profits compred to last year. $" + str((int(lst[8])-csh)) + " less")
            else:
                print("There is no Reduce of profits Compared to last year")
        if Mth == "O":
            if csh < int(lst[9]):
                print("There is a reduce in profits compred to last year. $" + str((int(lst[9])-csh)) + " less")
            else:
                print("There is no Reduce of profits Compared to last year")
        if Mth == "N":
            if csh < int(lst[10]):
                print("There is a reduce in profits compred to last year. $" + str((int(lst[10])-csh)) + " less")
            else:
                print("There is no Reduce of profits Compared to last year")
        if Mth == "D":
            if csh < int(lst[11]):
                print("There is a reduce in profits compred to last year. $" + str((int(lst[11])-csh)) + " less")
            else:
                print("There is no Reduce of profits Compared to last year")

main()
