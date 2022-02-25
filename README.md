# PB007_1966300_Gonzalez_Castillo_Cesar_Hiram

#include <iostream>

using namespace std;

int main()
{
    string nombre;
    string tratamiento;
    string descripcion;
    int cantidad;
    double hora;
    double unitario;
    double precio;
    double total;
    int opcion;
    int cita;
    
    do{
        cout<<"1 agendar cita   2 modificar cita    3 eliminar cita 4 lista de citas vigentes   5 limpiar pantalla  6 salir"<<endl;
        cin>>opcion;
    cita=cita+1;
        
        switch(opcion){
            case 1:
            cout<<"nombre del paciente"<<endl;
            cin>>nombre;
            
            cout<<"hora del tratamiento"<<endl;
            cin>>hora;
            
            cout<<"nombre del tratamiento"<<endl;
            cin>>tratamiento;
            
            cout<<"descripcion del tratamiento"<<endl;
            cin>>descripcion;
            
            cout<<"precio unitario del tratamiento"<<endl;
            cin>>unitario;
            
            cout<<"cantidad de tratamiento"<<endl;
            cin>>cantidad;
            
            cout<<"precio unitario"<<endl;
            cin>>precio;
            
            cout<<"total"<<endl;
            cin>>total;
            
            break;
            case 2:
            cout<<"nombre del paciente"<<endl;
            cin>>nombre;
            
            cout<<"hora del tratamiento"<<endl;
            cin>>hora;
            
            cout<<"nombre del tratamiento"<<endl;
            cin>>tratamiento;
            
            cout<<"descripcion del tratamiento"<<endl;
            cin>>descripcion;
            
            cout<<"precio unitario del tratamiento"<<endl;
            cin>>unitario;
            
            cout<<"cantidad de tratamiento"<<endl;
            cin>>cantidad;
            
            cout<<"precio unitario"<<endl;
            cin>>precio;
            
            cout<<"total"<<endl;
            cin>>total;
            
            break;
            case 3:
            
            
            break;
            case 4:
            
            
            break;
            case 5:
            
            
            break;
            case 6:
            
            
            default:
            cout<<"ingrese una opcion valida"<<endl;
        }
        while(opcion != 6)
        
    }
    
    return 0;
}
