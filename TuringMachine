package main;

public class maquinaTuring {

    char vetString[] = new char[99];
    int cabeca = 0;

    public void q0(char vetString[], int cabeca) {
        if (cabeca < vetString.length) {
            if (vetString[cabeca] == 'a') {
                vetString[cabeca] = 'X';
                cabeca = cabeca + 1;
                q1(vetString, cabeca);
            } else if (vetString[cabeca] == 'X') {
                cabeca = cabeca + 1;
                q0(vetString, cabeca);
            } else if (vetString[cabeca] == 'Y') {
                q3(vetString, cabeca);
            }
            else{
                System.out.println("Rejeitado em q0");
            }
        } else {
            System.out.println("Rejeitado em q0!");
        }
    }

    public void q1(char vetString[], int cabeca) {
        if (cabeca < vetString.length) {
            if (vetString[cabeca] == 'b') {
                vetString[cabeca] = 'Y';
                cabeca = cabeca + 1;
                q2(vetString, cabeca);
            } else if (vetString[cabeca] == 'Y') {
                cabeca = cabeca + 1;
                q1(vetString, cabeca);
            } else {
                cabeca = cabeca + 1;
                q1(vetString, cabeca);
            }

        } else {
            System.out.println("Rejeitado em q1");
        }

    }

    public void q2(char vetString[], int cabeca) {
        if (cabeca < vetString.length) {
            if (vetString[cabeca] == 'c') {
                vetString[cabeca] = 'Z';
//                cabeca = 0;
                q6(vetString, cabeca);

            } else if (vetString[cabeca] == 'Z') {
                cabeca = cabeca + 1;
                q2(vetString, cabeca);
            } else {
                cabeca = cabeca + 1;
                q2(vetString, cabeca);
            }
        } else {
            System.out.println("Rejeitado em q2");
        }
    }

    public void q5final(char vetString[], int cabeca) {
        System.out.println("Aceito");
    }

    public void q3(char vetString[], int cabeca) {
        if (vetString[cabeca] == 'Y') {
            cabeca = cabeca + 1;
            q3(vetString, cabeca);
        } else if (vetString[cabeca] == 'Z') {
            q4(vetString, cabeca);
        } else {
            System.out.println("Rejeitado em q3");
        }

    }

    public void q4(char vetString[], int cabeca) {
        if (cabeca != vetString.length) {
            if (vetString[cabeca] == 'Z') {
                cabeca = cabeca + 1;
                q4(vetString, cabeca);
            } else {
                System.out.println("Rejeitado em q4");
            }
        }else{
            System.out.println("Aceito!");
        }
    }
    public void q6(char vetString[],int cabeca){
        do{
            cabeca=cabeca-1;
        }while(cabeca!=0);
        q0(vetString,cabeca);
    }
    public char[] converteString(String string) {
        char vetString[] = new char[string.length()];
        vetString = string.toCharArray();
        return vetString;
    }

}
