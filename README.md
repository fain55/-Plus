file_path=input('the filename is')          #文件无空格(包括多行)

file_path=file_path

with open(file_path) as file_object:
    
    contents=file_object.read()
    contents=contents.rstrip()


message=contents

message=message.upper()

key=input('choose a number from 1 to 25')

key=int(key)

mode=input('attack or denfense = "1" or "2"')        #填写数字

mode=mode

outcome=''

may=''

Modes='ABCDEFGHIJKLMNOPQRSTUVWXYZ'

for sweet in message:
    
    if sweet in Modes:
        less=Modes.find(sweet)
    if mode=='2':
       less=less+key
    elif mode=='1':
        less=less-key
    if less >= len(Modes):
        less=less-len(Modes)
    if less <= 0:
        less=less+len(Modes)
    outcome=Modes[less]
    may+=outcome


print(may)
