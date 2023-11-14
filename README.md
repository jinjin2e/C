# 개인적으로 어려웠던 문법들 정리  

## 구조체 
> 구조체(struct)란 사용자가 C언어의 기본 타입을 가지고 새롭게 정의할 수 있는 사용자 정의 타입입니다.  
> 배열이 같은 타입의 변수 집합이라고 한다면, 구조체는 다양한 타입의 변수 집합을 하나의 타입으로 나타낸 것입니다.  
> 이때 구조체를 구성하는 변수를 구조체의 멤버(member) 또는 멤버 변수(member variable)라고 합니다.  
>
> struct book // 구조체의 선언, 사용할 멤버들 선언을 해준다.  
> {  
>    char title[30];  
>    char author[30];  
>    int price;  
> };    
> int main(void)  
> {  
>    struct book my_book = {"HTML과 CSS", "홍길동", 28000};   // struct book 과 같은 구조를 사용하는 my book 이라는 변수를 만듦 > my book의 값을 설정   
>    struct book java_book = {.title = "Java language", .price = 30000}; // struct book 의 구조로 java_book 이라는 변수를 만듦, 형식만 book 의 형식을 가져와 새로 만들어 my_book 변수와는 별개의 변수이기때문에 멤버의 값을 공유하지 않음(별개의 변수임)   
>   
>    printf("첫 번째 책의 제목은 %s이고, 저자는 %s이며, 가격은 %d원입니다.\n",  
>        my_book.title, my_book.author, my_book.price);    
>          
>    printf("두 번째 책의 제목은 %s이고, 저자는 %s이며, 가격은 %d원입니다.\n",  
>        java_book.title, java_book.author, java_book.price); // 초기화를 하면서 java_book 구조체 변수의 멤버 중 .author 은 정의하지 않았기 때문에 0이 들어가있음.  
>
>    return 0;  
> }
> 결과  
> 첫 번째 책의 제목은 HTML과 CSS이고, 저자는 홍길동이며, 가격은 28000원입니다.  
> 두 번째 책의 제목은 Java language이고, 저자는 이며, 가격은 30000원입니다.  

