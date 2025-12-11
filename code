# -*- coding: utf-8 -*-

import os
import time

#ANSII Fonts:
BOLD = "\033[1m"
ITALIC_STYLE =  "\033[3m"
#ANSII colors:
RESET = "\033[0m"
RED = "\033[31m"
GREEN = "\033[32m"
YELLOW = "\033[33m"
BLUE = "\033[34m"
PURPLE = "\033[35m" 
CYAN = "\033[36m"
WHITE = "\033[37m"

#title: 
TITLE = "_______PU_PAISII_HILENDARSKI_______  "
#database for faculties:
PU_FACULTIES = {
    1: ["Faculty of Mathematics and Informatics"],
    3: ["Faculty of Philology"],
    4: ["Faculty of Biology"],
    5: ["Faculty of Chemistry"],
    6: ["Faculty of Pedagogy"],
    7: ["Faculty of Law"],
    8: ["Faculty of Economic and Social Sciences"],
    9: ["Faculty of Philosophy and History"],
    13: ["Faculty of Physics and Technology"]
}

#database for specialities:
PU_SPECIALITIES = {
    126: ["Informatics", True, True],
    156: ["Business Information Technologies", True, True],
    168: ["Software Technologies and Design", True, True],
    132: ["Software Engineering", True, True],
    105: ["Mathematics", True, False],
    139: ["Business Mathematics", True, False],
    123: ["Applied Mathematics", True, False],
    118: ["Mathematics, Informatics and Information Technologies", True, False],
    165: ["Information Technologies, Mathematics and Educational Management", True, False],
    154: ["Artificial Intelligence", True, False],
    155: ["Information and Network Security", True, False],
    301: ["Bulgarian Philology", True, True],
    304: ["English Philology", True, False],
    302: ["Russian Philology", True, True],
    376: ["French Philology", True, False],
    303: ["Slavistics", True, False],
    358: ["Linguistics with IT", True, False],
    371: ["Applied Linguistics (English)", True, False],
    372: ["Applied Linguistics (German)", True, False],
    382: ["Applied Linguistics (French)", True, False],
    381: ["Applied Linguistics (Spanish)", True, False],
    380: ["Linguistics with Marketing", True, False],
    392: ["Linguistics with Business Administration", True, False],
    313: ["Bulgarian and English", True, False],
    315: ["Bulgarian and German", True, False],
    316: ["Bulgarian and French", True, False],
    398: ["Bulgarian and Information Security", True, False],
    317: ["Bulgarian Language and History", True, True],
    351: ["Bulgarian and Modern Greek", True, False],
    312: ["Bulgarian and Russian", True, True],
    348: ["Bulgarian and Turkish", True, False],
    370: ["Bulgarian and Chinese", True, False],
    386: ["Bulgarian and Italian", True, False],
    387: ["Bulgarian and Korean", True, False],
    320: ["Bulgarian, Civic Education and Philosophy", True, False],
    378: ["English and Cultural Heritage", True, False],
    408: ["Biology", True, True],
    454: ["Medical Biology", True, False],
    438: ["Molecular Biology", True, False],
    428: ["Microbiology and Virology", True, False],
    490: ["Pharmaceutical Biotechnology", True, True],
    409: ["Ecology and Environmental Protection", True, True],
    488: ["Biology and English", True, False],
    422: ["Biology and Chemistry", True, False],
    418: ["Biology and Physical Education", True, False],
    419: ["Pedagogy of Physical Education", True, True],
    557: ["Medical Chemistry", True, False],
    507: ["Chemistry", True, True],
    511: ["Chemistry with Marketing", True, False],
    577: ["Chemical Analysis and Quality Control", True, False],
    569: ["Forensic Chemistry", True, False],
    550: ["Chemistry and English", True, False],
    624: ["Pedagogy", True, False],
    610: ["Preschool Pedagogy", True, False],
    640: ["Preschool Pedagogy and Foreign Language", True, False],
    614: ["Primary School Pedagogy", True, False],
    641: ["Primary School Pedagogy and Foreign Language", True, False],
    642: ["Preschool and Primary School Pedagogy", True, True],
    630: ["Social Pedagogy", True, False],
    629: ["Special Pedagogy", True, False],
    655: ["Psychology", True, True],
    631: ["Social Work", True, False],
    669: ["Graphic Design with Advertising", True, False],
    695: ["Jazz and Pop Performance", True, False],
    691: ["Music", True, False],
    667: ["Acting for Drama Theatre", True, False],
    696: ["Art Education Pedagogy", True, False],
    697: ["Music Education Pedagogy", True, False],
    725: ["Law", True, False],
    845: ["Marketing", True, True],
    846: ["Business Management", True, True],
    899: ["National Security", True, True],
    844: ["Political Science", True, False],
    831: ["Economics and Business", True, True],
    834: ["International Economic Relations", True, False],
    893: ["Finance", True, True],
    878: ["Public Administration", True, True],
    894: ["Accounting", True, True],
    862: ["Management of Tourism Business", True, True],
    927: ["History", True, True],
    935: ["Archaeology", True, False],
    929: ["Document Studies and Archival Studies", True, False],
    930: ["History and Cultural Heritage", True, False],
    961: ["Cultural and Social Anthropology", True, False],
    975: ["Sociology of Law, Economics and Innovation", True, False],
    985: ["Sociology and Human Sciences", True, False],
    963: ["Cultural Tourism", True, False],
    936: ["Theology", True, False],
    928: ["Philosophy", True, False],
    989: ["European Studies, Programs and Projects", True, False],
    974: ["History and Foreign Language", True, False],
    980: ["Civic Education, Philosophy and Foreign Language", True, False],
    977: ["Geography, Technologies and Entrepreneurship", True, False],
    1306: ["Engineering Physics", True, True],
    1313: ["Medical Technologies", True, False],
    1323: ["Telecommunication Technologies", True, True],
    1360: ["Eco-Energy Technologies", True, False],
    1314: ["Telecommunication Engineering", True, False],
    1337: ["Telecommunications with Management", True, False],
    1381: ["Information and Computer Engineering", True, False],
    1364: ["Hardware and Software Systems (Smolyan)", True, False],
    1385: ["Automotive Engineering (Smolyan)", True, False],
    1315: ["Computer Industrial Engineering (Smolyan)", True, False],
    1387: ["Power Supply and Electrical Equipment (Smolyan)", True, False],
    1333: ["Automotive and Electronic Systems (Smolyan)", True, False],
    1388: ["Information and Computer Engineering with Management (Smolyan)", True, False],
    1321: ["Science Education for Lower Secondary School", True, True]
}
#printing program's info: 
def info():
    print(BLUE+ITALIC_STYLE+TITLE+RESET)
    print(YELLOW+"When entering a student's faculty number,"
       +"the program displays the faculty, specialty and form of study,"
       +"to exit the program type esc or ESK."
       +"Specialties from the Lyuben Karavelov branch in Kardzhali are not included"
       +"Enter uni number:"+RESET,end="")
#message if uni number is not valid: 
def excetion_message():
    print(RED+"Invalid number!"+RESET)
    time.sleep(2) 
#func for catching exceptions: 
def check_for_exceptions(uni_number):
    if len(uni_number) != 10:
      return True
    try:
      int(uni_number)
    except TypeError:
      return True
    except ValueError:
      return True
    return False
#2501261030
#func for get faculty: 
def get_faculty(uni_number):
    fac_code = int(uni_number[2]+uni_number[3])
    result = PU_FACULTIES.get(fac_code)
    if result is None:
        return ""
    return result[0]

#func for get speciality:
def get_speciality(uni_number):
    code = int(uni_number[2]+uni_number[3]+uni_number[4]+uni_number[5])
    if code in PU_SPECIALITIES:
       return PU_SPECIALITIES[code][0]
    return ""
#func for get form of education: 
def get_mode(uni_number):
   code = int(uni_number[3:6])
   if code not in PU_SPECIALITIES:
      return ""

   mode = uni_number[6]
   name, is_regular, external = PU_SPECIALITIES[code]

   if code != 725:
      if mode == '1' and is_regular:
        return "Regular"
      if mode == '2' and external:
        return "External"
   else:
      if mode == '3':
        return "Regular"

   return ""
#func for main operation: 
def program():
   while True:
     os.system("cls")
     info()
     #break option: 
     uni_number = input()
     if uni_number == "esc":
        break

     #exception check: 
     if check_for_exceptions(uni_number):
        excetion_message()
        continue

     faculty = get_faculty(uni_number)
     speciality = get_speciality(uni_number)
     mode = get_mode(uni_number)
     #check for invalid: 
     if faculty == "" or speciality == "" or mode == "":
        excetion_message()
        continue
    #result: 
     print(YELLOW+"Faculty:"
       +RESET,GREEN+faculty+RESET)
     print(YELLOW+"Speciality:"
       +RESET,GREEN+speciality+RESET)
     print(YELLOW+"Form of education:"
       +RESET,GREEN+mode+RESET)
     time.sleep(4)
#run program:    
program()

