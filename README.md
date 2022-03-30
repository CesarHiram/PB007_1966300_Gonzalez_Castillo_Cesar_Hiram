# PB007_1966300_Gonzalez_Castillo_Cesar_Hiram

#include <iostream>
#include <string>

using namespace std;

struct citas
{
   int numcita;
   string nombre;
    string tratamiento;
    string descripcion;
    int cantidad;
    double hora;
    double unitario;
    double precio;
    double total;

};

int main()
{
    citas cita[3];
    string nombre;
    string tratamiento;
    string descripcion;
    int cantidad;
    double hora;
    double unitario;
    double precio;
    double total;
    int opcion;
    int i;
    int j;
    
    do
    {
        cout<<"1 agendar cita   2 modificar cita    3 eliminar cita 4 lista de citas vigentes   5 limpiar pantalla  6 salir"<<endl;
        cin>>opcion;
        
        switch(opcion)
        {
            case 1:
            for (i=0;i<3;i++)
        {
            cout<<"nombre del paciente"<<endl;
            cin>>cita[i].nombre;
            
            cout<<"hora del tratamiento"<<endl;
            cin>>cita[i].hora;
            
            cout<<"nombre del tratamiento"<<endl;
            cin>>cita[i].tratamiento;
            
            cout<<"descripcion del tratamiento"<<endl;
            cin>>cita[i].descripcion;
            
            cout<<"precio unitario del tratamiento"<<endl;
            cin>>cita[i].unitario;
            
            cout<<"cantidad de tratamiento"<<endl;
            cin>>cita[i].cantidad;
            
            cout<<"precio unitario"<<endl;
            cin>>cita[i].precio;
            
            cout<<"total"<<endl;
            cin>>cita[i].total;
        }
            
            
            break;
            case 2:
            printf("numero de cita que desea modificar");
        cin>>j;
        j=j-1; //1-1=0
        for (i=j;i<=j;i++)
        {
         cout<<"nombre del paciente"<<endl;
            cin>>cita[i].nombre;
            
            cout<<"hora del tratamiento"<<endl;
            cin>>cita[i].hora;
            
            cout<<"nombre del tratamiento"<<endl;
            cin>>cita[i].tratamiento;
            
            cout<<"descripcion del tratamiento"<<endl;
            cin>>cita[i].descripcion;
            
            cout<<"precio unitario del tratamiento"<<endl;
            cin>>cita[i].unitario;
            
            cout<<"cantidad de tratamiento"<<endl;
            cin>>cita[i].cantidad;
            
            cout<<"precio unitario"<<endl;
            cin>>cita[i].precio;
            
            cout<<"total"<<endl;
            cin>>cita[i].total;
        }
            
            break;
            case 3:
            
            
            break;
            case 4:
            for(i=0;i<3;i++)
        { 
           cout<<"numero cita: "<<i+1<<endl;
             cout<<cita[i].nombre<<endl;
             cout<<cita[i].hora<<endl;
             cout<<cita[i].tratamiento<<endl;
             cout<<cita[i].descripcion<<endl;
             cout<<cita[i].unitario<<endl;
             cout<<cita[i].cantidad<<endl;
             cout<<cita[i].precio<<endl;
             cout<<cita[i].total<<endl;
        }
            
            break;
            case 5:
            system("cls");
            
            break;
            case 6:
            
            
            default:
            cout<<"ingrese una opcion valida"<<endl;
        }
    }    
        
        while(opcion != 6);
        
    
    
    return 0;
}
