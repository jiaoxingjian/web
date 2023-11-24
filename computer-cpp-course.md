# computer c++ course

## online tools

- https://www.onlinegdb.com/online_c++_compiler

## question 

- what is solid pricipal  closed to modification/open to extension
- basic building block
- how to build layer by layer

## design pattern

- https://sourcemaking.com/design_patterns

## code sample



- cpp class

  ```
  #include <iostream>
  
  using namespace std;
  
  class test
  {
  public:
      test();
      ~test();
      int getAge();
  private:
      int m_age;
      
  };
  
  test::test(){
    cout<<"test constructor"<<endl;
      //m_age=age;
  }
  test::~test(){
      cout<<"test destructor"<<endl;
  }
  int test::getAge()
  {
      return m_age;
  }
  
  
  int main()
  {
      int i;
      test t; //内存分配在stack。
      test *  ptest= new test[5];
      delete []ptest;
      int * p = new int[5];//new分配的内存在heap，
      delete []p;
      
    
      return 0;
  }
  ```

  - 学习重点， 构造函数的语法，使用，调用时机，对象的生成方式对应不同的内存分配方式
  - reference https://www.geeksforgeeks.org/how-to-initialize-array-of-objects-with-parameterized-constructors-in-c/

- pure abstract base class/ abstract base class (abc)  /multiple inheritance.

  ```
  #include <iostream>
  class food{
  public:
    virtual int getNutrition()=0;
  };
  
  class commodity{
  public:
      virtual float getPrice() = 0;
  };
  
  class huluobo :public food, public commodity
  {
  public:
      int getNutrition(){
          return 1;
      }
      float getPrice(){
          return 2.5;
      }
  };
  class tudou :public food
  {
  private:
  int color;    
  public:
      int getNutrition(){
          return 2;
      }
  };
  class chicken :public food
  {
  public:
      int getNutrition(){
          return 3;
      }
  };
  
  using namespace std;
  
  int main()
  {
      cout<<"total nutrition :";
      food *p1 = new huluobo();
      food *p2 = new tudou();
      food *p3 = new chicken();
      int total = p1->getNutrition()+p2->getNutrition()+p3->getNutrition();
      cout<<total<<endl;
      return 0;
  }
  ```

- c++ template method 

  https://www.youtube.com/watch?v=WN1GYmTmjfo

  https://sourcemaking.com/design_patterns/template_method/cpp/1



- https://www.google.com.hk/search?q=SFML+%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90&oq=SFML++%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90&aqs=chrome..69i57.10322j0j7&sourceid=chrome&ie=UTF-8
- https://medium.com/achiev/game-from-scratch-with-c-and-sfml-3-bbcdde38c3af

## design pattern

- http://www.vishalchovatiya.com/template-method-design-pattern-in-modern-cpp/
- https://www.youtube.com/playlist?list=PLvv0ScY6vfd9wBflF0f6ynlDQuaeKYzyc