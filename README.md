# last_step
#Вводим число состоящее из N цифр
ks = input()
#Создаём два пустых массива, чтобы засунуть туда первую и вторую часть числа
perwaya = []
vtoraya = []
#Заполняем массивы, сортируем значения по возрастанию/убыванию
for i in range(len(ks)//2):
    perwaya.append(ks[i])
for i in range(len(ks)//2, len(ks)):
    vtoraya.append(ks[i])
perwaya.sort()
vtoraya.sort()

#Создаём пустую строку и проверяем условие задачи
stroka = ''
for i in range(len(ks)//2):
    if perwaya[i] > vtoraya[i]:
        stroka += '1'
    else:
        stroka += '0'
#Если условие выполняется выводим YES, иначе выводим NO
if stroka == '1'*(len(ks)//2) or stroka == '0'*(len(ks)//2):
    print('YES')
else:
    print('NO')
        
