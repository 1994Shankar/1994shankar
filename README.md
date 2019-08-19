'''Python program to check the PID file and REQ file are present or not inside the perticular path, if it's present it will delete it '''


import os

def pid():

    path1 = "C:\prints\PID"

    print("PID FOLDER")
    if len(os.listdir(path1)) == 0:
        print("------------directory is empty------------------")

    else:
        print("----Folder is not empty-----")
        file_name = os.listdir(path1)
        os.chdir(path1)
        print("changing the path to:----->", os.getcwd())
        for new_file in file_name:
            print(new_file)
            os.remove(new_file)
            print("Its Deleted")


def Req():

    path2 = "C:\prints\REQS"
    
    print("REQ FOLDER")
    if len(os.listdir(path2)) == 0:
        print("-----------------directory is empty-------------------")

    else:
        print("------folder is not empty--------")
        file_name = os.listdir(path2)
        os.chdir(path2)
        print("changing the path to:------>", os.getcwd())
        for new_file in file_name:
            print(new_file)
            os.remove(new_file)
            print("its deleted")


pid()
Req()
