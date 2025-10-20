# Simple-Python-Conversational-Bot-chatbot-
تطبيق بسيط باستخدام لغة بايثون لتحليل المدخلات النصية و جمع معلومات المستخدم (الاسم ، العمر، البلد، الهواية) يهدف إلى بناء محادثة تفاعلية مخصصة للمستخدم
name = input("Hello, what's your name?\n")
if "name is" in name.lower():
    name = name.lower().split("name is")[-1].strip().title()
elif "i'm" in name.lower():
    name= name.lower().split("i'm")[-1].strip().title()
elif "i am" in name.lower():
    name = name.lower().split("i am")[-1].strip().title()
else:
    name = name.title()
print(f"welcome {name}")
country = input(f"where are you from {name}?\n")
if "from" in country.lower():
    country = country.lower().split("from")[-1].strip().title()
else:
    country = country.title()
print(f"It's my pleasure to meet someone from {country}, {name}")
age =eval(input(f"how old are you {name}?\n"))
if age < 18:
    print(f"you are still in school {name}, right?")
elif age > 35:
    print(f"really?! you don't look a day over {age}, {name}!")
else:
    print(f"great!! you still can do many things in your life {name}!")
hobby = input(f"what do like to do in your free time {name}?\n")
if "like to" in hobby.lower() and "ing" not in hobby.lower():
    hobby = hobby.lower().split("like to")[-1].strip()+"ing"
elif "love to" in hobby.lower() and "ing" not in hobby.lower():
    hobby = hobby.lower().split("love to")[-1].strip()+"ing"
elif "prefer to" in hobby.lower and "ing" not in hobby.lower():
    hobby = hobby.lower().split("prefer to")[-1].strip()+"ing"
elif "ing" not in hobby.lower():
    hobby = hobby + "ing"
else:
    hobby = hobby.lower()
print(f"great! {hobby} is an intersting activity {name}, to do in your free time ")
feel = input(f"Did you enjoy this conversation {name}?\n")
print(f"Me too! thanks for it {name}")