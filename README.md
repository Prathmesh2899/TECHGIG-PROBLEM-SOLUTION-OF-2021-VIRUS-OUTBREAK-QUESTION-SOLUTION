# TECHGIG-PROBLEM-SOLUTION-OF-2021-VIRUS-OUTBREAK-QUESTION-SOLUTION
# This Solution For Java Lover's

public static void isCOVIDTest(Scanner scanner) {
if (scanner != null) {
String strV = scanner.next().toLowerCase().trim();
int number = scanner.nextInt();
int i = 2;
while ( i < (number+2)){
String strB = scanner.next().toLowerCase().trim();
doTest(strV, strB);
i++;
}
}else {
System.out.println("NEGATIVE");
}
}

public static void doTest(String strV, String strB){
int vLenght = strV.length();
int bLenght = strB.length();
if (vLenght >= bLenght) {
int indexV = 0;
int indexB = 0;
while (indexB < bLenght && indexV < vLenght ) {
if (strB.charAt(indexB) == strV.charAt(indexV)) {
indexB += 1;
}
indexV += 1;
}
if (indexB == bLenght){
System.out.println("POSITIVE");
return;
}
}
System.out.println("NEGATIVE");
}
