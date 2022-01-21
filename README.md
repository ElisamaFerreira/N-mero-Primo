# N-mero-Primo
Verificação simples de Número Primo

#include <iostream>
#include <locale>

using namespace std;

int main()
{

    int num = 0, i = 0, result = 0, primo = 0, mult_3 = 0;
    string encerrar = "";

setlocale(LC_ALL, "portuguese");

    do{
        cout << "Por gentileza, informe um número: ";
        cin >> num;

        for (i = 2; i <= num / 2; i++) {
            if (num % i == 0){
                result++;
                break;
            }
        }

        if (result == 0){
            primo++;
            cout << "Este número é primo!" << endl;
        }else{
            cout << "Este número não é primo!" << endl;
        }

        if (num % 3 == 0){
            mult_3++;
            cout << "O número informado é multiplo de 3!" << endl;
            
        }else{
            cout << "O número informado não é multiplo de 3!" << endl;
        }

        cout << "Gostaria de continuar? {S/N}" << endl;
        cin >> encerrar;
        cout << ('\n');
        
    } while (encerrar == "S" || encerrar == "s");

    //Resultado 
    cout << "Os números Primos são: " << primo << endl;
    cout << "Quantidade de Multiplos de 3: " << mult_3 << endl;

    return 0;
}
