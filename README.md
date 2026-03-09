def add_book():
    title = input("Enter book title: ")
    status = input("Enter status (Reading / Read / TBR): ) ")
    
    book = {
        "title": title,
        "status": status,
        "quotes": []
    }
    
    books. append(book)
    print("Book added successfully!\n")
    
    def view_books():
        if not books:
            print("No books added yet.\n")
            return
            
    for i, book in enumerate(books):
        print(f"{i+1}. {book['title']} ({book['status]']})")
    print()
    
def main_menu():
    while True:
        print("==== BOOK TRACKER ====")
        print("1. Add Book")
        print("2. View Books")
        print("3. Add Quote/Flashcard")
        print("4. Study Flashcards")
        print ("5. Exit")
            
        choice = input("Choose and option: ")
            
        if choice == "1":
            add_book()
        elif choice == "2":
            view_books()
        elif choice == "3":
            add_quote()
        elif choice == "4":
            study_flashcard()
        elif choice == "5":
            print("Goodbye!")
            break
        else:
            print("Invalid choice.\n")
                
def main_menu():
    while True:
        print("Hello")
        break
        
main_menu()

def add_quote():
    # Step 1: Check if there are any books first
    if not books:
        print("You need to add book before you can add a quote!\n")
        return
        
    # Step 2: Show the user their book so they can pcik one
    print("Select a book to extract a quote from")
    for i, book in enumerate(books):
        print(f"{i+1}. {book['title']}")
        
    # Step 3: Get the user's choice
    index = int(input("enter the book number: ")) - 1
    
    # Step 4: Ask for the quote/info
    new_quote = input("Enter the quote or info you want to recall: ")
    
    # Step 5: Save it into that specific book's "quotes" list
    books[index]["quotes"].append(new_quote)
    
    print("Quote saved and flashcard created!\n")
    
def study_flashcards():
    if not books: 
        print ("No books found. Add some books and quotes first!\n")
        return
        
    print("\n--- FLASHCARD STUDY SESSION ---")
    for book in books:
        if not book["quotes"]:
            continue
            
        for quote in book["quotes"]:
            print(f"\nBOOK: {book['title']}")
            input("press Enter to study the flashcard...")
            print(f">>>{quote}")
            print("-" * 30)
            
        print("\nEnd of session!\n")
        print("HELLO WORLD")
        
main_menu
