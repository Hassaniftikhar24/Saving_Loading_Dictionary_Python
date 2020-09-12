Task: 2 tasks, (1) Save a dictionary (2) Retrieve that same dictionary to get the data
Task_1: Write a python function to save a dictionary to a file
Input_1 : Dictionary to be saved, output file path
Output_1 : Saving that dictionary

Task_2: Write a python function to sort the words in a string
Input_2: file path to saved dictionary
Output_2: return the retrieved dictionary object

# Task 01
dictionary_save = {
    "Name": "Hassan",
    "Age": "28",
    "Location": "Tampere",
    "Country": "Finland"
}
file_path = "E:\Python\Projects\dictionary_save_retrieve\dictionary_to_be_saved"
def save_dictionary(dict_write, choosen_file_path):

    f = open(choosen_file_path, "w")
    f.write(str(dict_write))
    f.close()
    return choosen_file_path

# Task 02
def load_dictionary(dict_read):
    f = open(dict_read, "r")
    data = f.read()
    f.close()
    return eval(data)

x = save_dictionary(dictionary_save, file_path)
y=load_dictionary(x)
print(y)
