PPS C MINI PROJECT - RA2111037010037


      #include <stdio.h>
    #include <stdlib.h>
    #include <string.h>
    struct library {
    char book_name[70];
    char author[70];
    int pages;
    float price;
     };

     int main(){ 
     struct library lib[100];
    char ar_nm[100], bk_nm[100];

    int i, input, count;
    i = input = count = 0;
  
    while (input != 5) {
  
        printf("\n\n*###### WELCOME TO E-LIBRARY #####*\n");
        printf("\n\n1. Add book information\n2. Display book information\n");
        printf("3. List all books of given author\n");
        printf("4. List the count of books in the library\n");
        printf("5. Exit");
  
        // Enter the book details
        printf("\n\nEnter one of the above: ");
        scanf("%d", &input);
  
        // Process the input
        switch (input) {
  
        // Add book
        case 1:
  
            printf("Enter book name = ");
            scanf("%s", lib[i].book_name);
  
            printf("Enter author name = ");
            scanf("%s", lib[i].author);
  
            printf("Enter pages = ");
            scanf("%d", &lib[i].pages);
  
            printf("Enter price = ");
            scanf("%f", &lib[i].price);
            count++;
  
            break;
  
        // Print book information
        case 2:
            printf("You have entered the following information : \n");
            for (i = 0; i < count; i++) {
                printf("Book name = %s", lib[i].book_name);
                printf("\nAuthor name = %s", lib[i].author);
                printf("\nPages = %d", lib[i].pages);
                printf("\nPrice = %f", lib[i].price);
            }
            break;
  
        // Take the author name as input
        case 3:
            printf("Enter author name : ");
            scanf("%s", ar_nm);
            for (i = 0; i < count; i++) {
  
               if (strcmp(ar_nm, lib[i].author) == 0) {
                printf("Book name = %s", lib[i].book_name);
                printf("\nAuthor name = %s", lib[i].author);
                printf("\nPages = %d", lib[i].pages);
                printf("\nPrice = %f", lib[i].price); }
                else {printf("\nAuthor not found"); }
            }
            break;
  
        // Print total count
        case 4:
            printf("\n No of books in library : %d",count);
            break;
            
        case 5:
            exit(0);
        }
       // l: printf("\nAuthor not found");
    }
    
    return 0;
    }
