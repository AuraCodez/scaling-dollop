from operator import add 
new_list = []
while True:
    inp = input('Enter the  exam and programming exercise results: ')
    if inp:
        x, y = inp.split()
        new_list.append(x)
        new_list.append(y)
    else:
        print("----Statistics----")
        
        program_exercises = new_list[1::2] 
        for items in range(0,len(program_exercises)):
            program_exercises[items] = int(program_exercises[items]) 
        program_points = []    
        for items in program_exercises:
            program_points.append(items/10)
                           
        
        points = new_list[0::2] 
        for items in range(0,len(points)):
            points[items] = int(points[items]) 
        
        result = list(map(add, points, program_points))  
        average_points = sum(result)/len(result)
        print(f"Points average : {average_points:.2f}")
        
        counter = 0
        for items in result:
            if items <= 14:
                counter = counter + 1
                percentage = ((len(result) - counter)/len(result)) * 100
            elif items >= 15:
                percentage = ((len(result) - counter)/len(result)) * 100
        print(f"Pass percentage : {percentage:.2f}")
        
        print("Grade distrubition:")
        fail_list = []
        grade_1 = []
        grade_2 = []
        grade_3 = []
        grade_4 = []
        grade_5 = []
        out_of_bounds = []
        for items in result:
            if items <= 0:
                out_of_bounds.append(items)
            elif items >0 and items <=14.99:
                fail_list.append(items)
            elif items >=15 and items <=17.99:
                grade_1.append(items)
            elif items >= 18 and items <=20.99:
                grade_2.append(items)
            elif items >= 21 and items <=23.99:
                grade_3.append(items)
            elif items >= 24 and items <= 27.99:
                grade_4.append(items)
            elif items >= 28 and items <= 30.99:
                grade_5.append(items)
            elif items > 30:
                out_of_bounds.append(items)
            
                
                
        print("0:" + len(fail_list) * "*")
        print("1:" + len(grade_1) * "*")
        print("2:" + len(grade_2) * "*")
        print("3:" + len(grade_3) * "*")
        print("4:" + len(grade_4) * "*")
        print("5:" + len(grade_5) * "*")
        print("OBB grade:" + len(out_of_bounds) * "*")

                
        break
input("Press enter to close the program. . . .")
