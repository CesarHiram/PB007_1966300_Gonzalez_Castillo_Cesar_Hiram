# PB007_1966300_Gonzalez_Castillo_Cesar_Hiram

#include <iostream>
#include <conio.h>
#include <string.h>
#include <string>
#include <fstream>
#include<stdlib.h>
#include <vector>

using namespace std;

void Alta();
void listas();
void archivos();
void eliminar();
void modificar();

int alta, * cantidad;
string * nombre, * tratamiento, * descripcion;
double * hora, *unitario, * precio, * total;
int main()
{
	int opc;
	cout << "1.-Alta" << endl << "2.- mostrar" << endl << "3.- limpiar pantalla" << endl<<"4.-Modificar"<<endl<<"5.-Eliminar"<<endl<<"6.-Salir"<<endl;
	cin >> opc;

	switch (opc)
	{
	case 1:
		Alta();
		return main();
		break;

	case 2:
		listas();
		return main();
		break;

	case 3:
		system("cls");
		return main();
		break;

	case 4:
		modificar();
		return main();
		break;

	case 5:
		eliminar();
		return main();
		break;

	case 6:
		archivos();
		break;
	}
}

void Alta()
{ 
	cout << "Digite el num de registros que desea dar de alta" << endl;
	cin >> alta;
	cantidad = new int[alta];
	nombre = new string [alta];
	tratamiento = new string [alta];
	descripcion = new string [alta];
	hora = new double[alta];
	unitario = new double[alta];
	precio = new double[alta];
	total = new double[alta];
	for (int i = 0;i < alta;i++)
	{
			
		while (getchar() != '\n');
		cout << "Ingrese nombre" << endl;
		getline(cin, nombre[i]);
		cout << "Ingrese el tratamiento" << endl;
		cin >> tratamiento[i];
		cout << "Ingrese la descripcion del tratamiento" << endl;
		cin >> descripcion[i];
		cout << "ingrese la hora del tratamiento" << endl;
		cin >> hora[i];
		cout << "ingrese el precio unitario del tratamiento" << endl;
		cin >> unitario[i];
		cout << "ingrese la cantidad del tratamiento" << endl;
		cin >> cantidad[i];
		cout << "ingresa el precio unitario" << endl;
		cin >> precio[i];
		cout << "ingresa el total a pagar" << endl;
		cin >> total[i];
		

	}
}

void listas()
{
	for (int i = 0;i < alta;i++)
	{
		cout << " registro" << i + 1 << endl;
		cout << nombre[i] << endl;
		cout << tratamiento[i] << endl;
		cout << descripcion[i] << endl;
		cout << hora[i] << endl;
		cout << unitario[i] << endl;
		cout << cantidad[i] << endl;
		cout << precio[i] << endl;
		cout << total[i] << endl;
	}
}

void archivos()
{
	ofstream archivo; 
	string nombrearchivo;
	int texto;
	string texto2;

	nombrearchivo = "altascitas";

	archivo.open(nombrearchivo.c_str(), ios::out);

	if (archivo.fail())
	{
		cout << "ERROR NO SE PUDO CREAR EL ARCHIVO";
		exit(1);
	}

	archivo << "NOMBRE" << "\t";
	archivo << "TRATAMIENTO" << "\t";
	archivo << "DESCRIPCION" << "\t";
	archivo << "HORA" << "\t";
	archivo << "UNITARIO" << "\t";
	archivo << "CANTIDAD" << "\n";
	archivo << "PRECIO" << "\n";
	archivo << "TOTAL" << "\n";

	for (int i = 0;i < alta;i++)
	{
		texto2 = nombre[i];
		archivo << texto2 << "\t"<< "\t";
		texto2 = tratamiento[i];
		archivo << texto2 << "\t" << "\t";
		texto2 = descripcion[i];
		archivo << texto2 << "\t " << "\t";
		texto = hora[i];
		archivo << texto << "\t "<< "\t";
		texto = unitario[i];
		archivo << texto << "\t "<< "\t";
		texto = cantidad[i];
		archivo << texto << "\t "<< "\t";
		texto = precio[i];
		archivo << texto << "\t "<< "\t";
		texto = total[i];
		archivo << texto << "\t "<< "\t";
		
	}


	archivo.close();
}

void eliminar()
{
	int j;
	cout << "ingrese el  registro a eliminar";
	cin >> j;
	j = j - 1;
	nombre = new string[alta];

	for (int i = j;i == j;i++)
	{
		nombre[i] = nombre[i + 1];
		tratamiento[i] = tratamiento[i + 1];
		descripcion[i] = descripcion[i + 1];
		hora[i] = hora[i + 1];
		unitario[i] = unitario[i + 1];
		cantidad[i] = cantidad[i + 1];
		precio[i] = precio[i + 1];
		total[i] = total[i + 1];
	}
}

void modificar()
{
	int j, opcion;
	 cout << "ingrese el numero registro a modificar";
	 cin >> j;
	 j = j - 1; 
	 cout << "ingrese que desea modificar 1.-Nombre,2.-Tratamiento, 3.-Descripcion, 4.-Hora, 5.-Unitario, 6.-Cantidad, 7.-Precio, 8.-Total" << endl;
	 cin >> opcion;

	 switch (opcion)
	 {
	 case 1:
		 for (int i = j;i == j;i++)
		 {
			 while (getchar() != '\n'); 
			 cout << "Ingrese nombre" << endl;
			 getline(cin, nombre[i]);
		 }
		 break;
	 case 2:
		 for (int i = j;i == j;i++)
		 {
			 cout << "Ingrese el tratamiento" << endl;
			 cin >> tratamiento[i];
		 }
		 break;

	 case 3:
		 for (int i = j;i == j;i++)
		 {
			 cout << "Ingrese la descripcion del tratamiento" << endl;
			 cin >> descripcion[i];
		 }
		 break;
		 
	 case 4:
	 for (int i = j;i == j;i++)
	    {
	         cout << "Ingrese la hora del tratamiento" << endl;
		     cin >> hora[i];
	    }
	    break;
	    case 5:
	    for (int i = j;i == j;i++){
	        cout << "Ingrese el precio unitario del tratamiento" << endl;
			 cin >> unitario[i];
	    }
	    break;
	    
	    case 6:
	    for (int i = j;i == j;i++){
	        cout << "Ingrese la cantidad" << endl;
			 cin >> cantidad[i];
	    }
	    break;
	    
	    case 7:
	    for (int i = j;i == j;i++){
	        cout << "Ingrese el precio unitario" << endl;
			 cin >> precio[i];
	    }
	    break;
	    
	    case 8:
	    for (int i = j;i == j;i++){
	        cout << "Ingrese el total a pagar" << endl;
			 cin >> total[i];
	    }
	 }

			
}


