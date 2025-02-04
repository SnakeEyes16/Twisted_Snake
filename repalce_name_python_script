import os

directory = input("Enter the directory path: ")

if not os.path.isdir(directory):
    print("Invalid directory.")
else:
    os.chdir(directory)
    files = [f for f in os.listdir(directory) if os.path.isfile(os.path.join(directory, f))]
    if not files:
        print("No files found in the directory.")
    else:
        print("Files in the directory:")
        for idx, file in enumerate(files, 1):
            print(f"{idx}. {file}")

        file_index = int(input("\nEnter the number of the file you want to rename: ")) - 1
        if file_index < 0 or file_index >= len(files):
            print("Invalid selection.")
        else:
            old_name = files[file_index]
            print(f"Selected file: {old_name}")
            new_name = input("Enter the new name for the file (with extension): ")
            os.rename(os.path.join(directory, old_name), os.path.join(directory, new_name))
            print(f"File renamed from {old_name} to {new_name}")
