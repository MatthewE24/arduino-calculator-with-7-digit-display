int one = 1, two = 2, three = 3, four = 4, five = 5, six = 6, seven = 7, eight = 8, nine = 9, ten = 10;
int btn = 13;
int btnVal = 0;
long number1;
long number2;
char calSignal;
long result;

void setup() {
  // put your setup code here, to run once:
  pinMode(one, OUTPUT);
  pinMode(two, OUTPUT);
  pinMode(three, OUTPUT);
  pinMode(four, OUTPUT);
  pinMode(five, OUTPUT);
  pinMode(six, OUTPUT);
  pinMode(seven, OUTPUT);
  pinMode(eight, OUTPUT);
  pinMode(nine, OUTPUT);
  pinMode(ten, OUTPUT);
  pinMode(btn,INPUT);
  Serial.begin(9600);
  Serial.println(" welcome to THE calculator");
  Serial.println("please input your desired calculation");
  Serial.println();
}

void loop() {
  // put your main code here, to run repeatedly:
    while(Serial.available() > 0) {
      number1 = Serial.parseInt();
      calSignal = Serial.read();
      number2 = Serial.parseInt();
      resultboi();
      Serial.println("result =");
      Serial.println(result);
      Serial.println();
        alloff();
        delay(3000);
        if (result == 0) zero();
      
        if (result == 1) displayone();
      
        if (result == 2) displaytwo();
      
        if (result == 3) displaythree();
      
        if (result == 4) displayfour();
       
        if (result == 5)  displayfive();
       
        if (result == 6) displaysix();
        
        if (result == 7) displayseven();
        
        if (result == 8) displayeight();
        
        if (result == 9) displaynine();

        if (result == 10) 
        {
          delay(1000);
          displayone();
          delay(1000);
          alloff();
          dash();
          delay(1000);
          alloff();
          zero();
          delay(1000);
        }

        if (result == 11)
        {
          delay(1000);
          displayone();
          delay(1000); 
          alloff();
          dash();
          delay(1000);
          alloff();
          displayone();
          delay(1000);
        }

        if (result == 12) 
           {
          delay(1000);
          displayone();
          delay(1000); 
          alloff();
          dash();
          delay(1000);
          alloff();
          displaytwo();
          delay(1000);
           }

        if (result == 13) 
         {
          delay(1000);
          displayone();
          delay(1000); 
          alloff();
          dash();
          delay(1000);
          alloff();
          displaythree();
          delay(1000);
        }

        if (result == 14) 
         {
          delay(1000);
          displayone();
          delay(1000); 
          alloff();
          dash();
          delay(1000);
          alloff();
          displayfour();
          delay(1000);
        }

        if (result == 15) 
         {
          delay(1000);
          displayone();
          delay(1000); 
          alloff();
          dash();
          delay(1000);
          alloff();
          displayfive();
          delay(1000);
        }

        if (result == 16) 
         {
          delay(1000);
          displayone();
          delay(1000); 
          alloff();
          dash();
          delay(1000);
          alloff();
          displaysix();
          delay(1000);
        }

        if (result == 17)
         {
          delay(1000);
          displayone();
          delay(1000); 
          alloff();
          dash();
          delay(1000);
          alloff();
          displayseven();
          delay(1000);
        }

        if (result == 18) 
         {
          delay(1000);
          displayone();
          delay(1000); 
          alloff();
          dash();
          delay(1000);
          alloff();
          displayeight();
          delay(1000);
        }

        if (result == 19) 
         {
          delay(1000);
          displayone();
          delay(1000); 
          alloff();
          dash();
          delay(1000);
          alloff();
          displaynine();
          delay(1000);
        }

        if (result == 20) 
         {
          delay(1000);
          displaytwo();
          delay(1000); 
          alloff();
          dash();
          delay(1000);
          alloff();
          zero();
          delay(1000);
        }
        
      Serial.println("Here you go!");
      Serial.println();
      Serial.println("you can keep going as long as you want");
      delay(3000);
      alloff();
      delay(3000);
    }
}

 
 
  
  
 /* displayone();
  delay(1000);
  alloff();
  delay(1000);
  displaytwo();
  delay(1000);
  alloff();
  delay(1000);
  displaythree();
  delay(1000);
  alloff();
  delay(1000);
  displayfour();
  delay(1000);
  alloff();
  delay(1000);
  displayfive();
  delay(1000);
  alloff();
  delay(1000);
  displaysix();
  delay(1000);
  alloff();
  delay(1000);
  displayseven();
  delay(1000);
  alloff();
  delay(1000);
  displayeight();
  delay(1000);
  alloff();
  delay(1000);
  displaynine();
  delay(1000);
  alloff();
  delay(1000);
}*/
void resultboi() {
  switch(calSignal) {
    case'+' :
    result = number1 + number2;
    break;
    case'-' :
    result = number1 - number2;
    break;
    case'*' :
    result = number1 * number2;
    break;
    case'/' :
    result = number1 / number2;
    break;
    default:("sorry, dont recognize that");
    Serial.println();
    result = 0;
  }
}
void zero() {
  //subroutine for the number zero
  digitalWrite(two, HIGH);
  digitalWrite(four, HIGH);
  digitalWrite(five, HIGH);
  digitalWrite(nine, HIGH);
  digitalWrite(seven, HIGH);
  digitalWrite(six, HIGH);
}
void displayone(){
  //subroutine for the number one
  digitalWrite(five, HIGH);
  digitalWrite(nine, HIGH);
}
void displaytwo() {
  //subroutine for the number two
  digitalWrite(four, HIGH);
  digitalWrite(five, HIGH);
  digitalWrite(one, HIGH);
  digitalWrite(six, HIGH);
  digitalWrite(seven, HIGH);
}
void displaythree() {
  //subroutine for three
  digitalWrite(four, HIGH);
  digitalWrite(five, HIGH);
  digitalWrite(one, HIGH);
  digitalWrite(nine, HIGH);
  digitalWrite(seven, HIGH);
}
void displayfour() {
  //subroutine for the number four
  digitalWrite(two, HIGH);
  digitalWrite(one, HIGH);
  digitalWrite(five, HIGH);
  digitalWrite(nine, HIGH);
}
void displayfive() {
  //subroutine for the number five
  digitalWrite(four, HIGH);
  digitalWrite(two, HIGH);
  digitalWrite(one, HIGH);
  digitalWrite(nine, HIGH);
  digitalWrite(seven, HIGH);
}
void displaysix() {
  //subroutine for the number six
  digitalWrite(four, HIGH);
  digitalWrite(two, HIGH);
  digitalWrite(one, HIGH);
  digitalWrite(six, HIGH);
  digitalWrite(seven, HIGH);
  digitalWrite(nine, HIGH);
}
void displayseven() {
  //subroutine for the number seven
  digitalWrite(four, HIGH);
  digitalWrite(five, HIGH);
  digitalWrite(nine, HIGH);
}
void displayeight() {
  //subroutine for the number eight
  digitalWrite(two, HIGH);
  digitalWrite(four, HIGH);
  digitalWrite(five, HIGH);
  digitalWrite(one, HIGH);
  digitalWrite(six, HIGH);
  digitalWrite(seven, HIGH);
  digitalWrite(nine, HIGH);
}
void displaynine() {
  //subroutine for the number nine
  digitalWrite(two, HIGH);
  digitalWrite(four, HIGH);
  digitalWrite(one, HIGH);
  digitalWrite(five, HIGH);
  digitalWrite(nine, HIGH);
}
void dot(){
  //subroutine for the dot
  digitalWrite(ten, HIGH);
}
void dash(){
  //subroutine for - 
  digitalWrite(one, HIGH);
}
void alloff() {
  //subroutine for all of them to shut off
  digitalWrite(one, LOW);
  digitalWrite(two, LOW);
  digitalWrite(four, LOW);
  digitalWrite(five, LOW);
  digitalWrite(six, LOW);
  digitalWrite(seven, LOW);
  digitalWrite(nine, LOW);
  digitalWrite(ten, LOW);
}











/*digitalWrite(four,HIGH);
  digitalWrite(five,HIGH);
  digitalWrite(one,HIGH);
  digitalWrite(six,HIGH);
  digitalWrite(seven,HIGH);
  delay(5000);
  digitalWrite(four,LOW);
  digitalWrite(five,LOW);
  digitalWrite(one,LOW);
  digitalWrite(six,LOW);
  digitalWrite(seven,LOW);
  delay(1000);*/
