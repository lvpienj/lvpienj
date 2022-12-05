#include <iostream>	
#include <string>
#include <stdlib.h>
using namespace std;


int main ()
{
	string name, gender, league, match, date, time;
	char  genderChoose, again, order, Class;
	int chooseLeague, chooseLaLigaMatch, economy = 1500000, VIP = 5000000;
	
	do{
		cout << "************************************************************************************************************" 	<< endl;
		cout << "	                   Welcome to the homepage of stadium's ticket purchase                                  "  << endl;
		cout << "************************************************************************************************************" 	<< endl;
		cout << endl;
			
		//People want to order ticket or no
		bool i = true;
		while (i) {
			cout << "Do you want to order the ticket? [y/n]" << endl; cin >> order;
			cout << endl;
			order = tolower(order);
			system ("cls");
				
			if (order == 'y'){
				i = false;
					
				// Input Data
					cout << "Please input your data : "<< endl	;
					cout << "Name                       = "			; cin >> name;
				bool j = true;
				while (j) {
					cout << "Gender([M]ale/ [F]emale)   = "			; cin >> genderChoose;
					cout << endl;
					genderChoose = tolower(genderChoose);
					if (genderChoose == 'm' ){
						j = false;
						gender ="Male";
					}
					else if (genderChoose == 'f') {
						j = false;
						gender = "Female";
					}
					else {
						j = true;
						cout << "Please input the right input" << endl;
					} system ("cls");
				}
				
				//Choose League
				cout << "Please select the league : " << endl;
				cout << "---------------------------------" << endl;
				cout << "|No. | League          |" << endl;
				cout << "---------------------------------" << endl;
				cout << "|1.  | La Liga         |" << endl;
				cout << "|2.  | Premier League  |" << endl;
				cout << "|3.  | Serie A Italia  |" << endl;
				cout << "---------------------------------" << endl;
				bool k = true;
				while (k) {
					cout << "Input your choice [1/2/3] = "; cin >> chooseLeague;
					cout << endl; system ("cls");
					
					//Choose Match
					if (chooseLeague == 1){
						k = false;
						league = "La Liga";
						cout << "You choose the La Liga" << endl;
						cout << "-------------------------------------------------------------" << endl;
						cout << "|No.	|Match                    |Date         |Time       |" << endl;
						cout << "-------------------------------------------------------------" << endl;							
						cout << "|1.	|Girona V Rayo            |2022/12/29	|23.00 WIB  |" << endl;
						cout << "|2.	|Betis V Bilbao           |2022/12/30	|01.15 WIB  |" << endl;
						cout << "|3.	|Atletico Madrid V Elche  |2022/12/30	|03.30 WIB  |" << endl;
						cout << "|4.	|Getafe V Mallorca        |2022/12/30	|23.00 WIB  |" << endl;
						cout << "|5.	|Celta V Sevilla          |2022/12/31	|01.15 WIB  |" << endl;
						cout << "|6.	|Cadiz V Almeria          |2022/12/31	|01.15 WIB  |" << endl;
						cout << "|7.	|Valladolid V Madrid      |2022/12/31	|03.30 WIB  |" << endl;
						cout << "|8.	|Barcelona V Espanyol     |2022/12/31	|20.00 WIB  |" << endl;
						cout << "|9.	|Real Sociedad V Osasuna  |2022/12/31	|22.15 WIB  |" << endl;
						cout << "|10.	|Villarreal V Valencia    |2022/12/31	|22.15 WIB  |" << endl;
						cout << "-------------------------------------------------------------" << endl;
						
						bool l = true;
						while (l){
							cout << "\n" << "Please Choose the match that you want to see" << endl;
							cin >> chooseLaLigaMatch;
							string LaLigaStadium[11] = {"", "Montilivi", "Benito Villamarin Stadium", "Wanda Metropolitano", "Alfonso Perez", "Balaidos Stadium", "Estadio Nuevo Mirandilla", "Nuevo Jose Zorrilla Stadium", "Camp Nou", "Anoeta Stadium", "Estadio Ciudad de Valencia"};
							if (chooseLaLigaMatch >= 0 && chooseLaLigaMatch <= 11) {
								l = false;
							}
							else if (chooseLaLigaMatch == 1) {
								match = "Girona V Rayo";
								date = "2022/12/29";
								time = "23.00 WIB";
							}
							else {
								l = true;
							}
						}
					}
					else if (chooseLeague == 2){                                               
						k = false;
						league = "Premier League";
						cout << "You choose the Premier League" << endl;
						cout << "-------------------------------------------------------------" << endl;
						cout << "|No.	|Match                      |Date       |Time       |" << endl;
						cout << "-------------------------------------------------------------" << endl;							
						cout << "|1.	|Brentford V Tottenham      |2022/12/26 |19.30 WIB  |" << endl;
						cout << "|2.	|Southampton V Brighton     |2022/12/26 |22.00 WIB  |" << endl;
						cout << "|3.	|Leicester V Newcastle      |2022/12/26 |22.00 WIB  |" << endl;
						cout << "|4.	|Crystal Palace V Fulham    |2022/12/26 |22.00 WIB  |" << endl;
						cout << "|5.	|Everton V Wolves           |2022/12/26 |22.00 WIB  |" << endl;
						cout << "|6.	|Aston Villa V Liverpool    |2022/12/27 |00.30 WIB  |" << endl;
						cout << "|7.	|Arsenal V West Ham         |2022/12/27 |03.30 WIB  |" << endl;
						cout << "|8.	|Chelsea V Bournemouth      |2022/12/28 |00.30 WIB  |" << endl;
						cout << "|9.	|Man Utd V Nottingham       |2022/12/28 |03.00 WIB  |" << endl;
						cout << "|10.	|Leeds V Man City           |2022/12/29 |03.00 WIB  |" << endl;
						cout << "-------------------------------------------------------------" << endl;
					}
					else if (chooseLeague == 3){
						k = false;
						league = "Serie A Italia";
						cout << "You choose the Serie A Italia" << endl;
						cout << "-------------------------------------------------------------" << endl;
						cout << "|No.	|Match                      |Date       |Time       |" << endl;
						cout << "-------------------------------------------------------------" << endl;							
						cout << "|1.	|Salernitana V Milan        |2022/01/04 |18.30 WIB  |" << endl;
						cout << "|2.	|Sassuolo V Sampdoria       |2022/01/04	|18.30 WIB  |" << endl;
						cout << "|3.	|Torino V Verona            |2022/01/04	|20.30 WIB  |" << endl;
						cout << "|4.	|Spezia V Atalanta          |2022/01/04	|22.30 WIB  |" << endl;
						cout << "|5.	|Roma V Bologna             |2022/01/04	|22.30 WIB  |" << endl;
						cout << "|6.	|Lecce V Lazio              |2022/01/04	|00.30 WIB  |" << endl;
						cout << "|7.	|Fiorentina V Monza         |2022/01/05	|00.30 WIB  |" << endl;
						cout << "|8.	|Cremonese V Juventus       |2022/01/05	|00.30 WIB  |" << endl;
						cout << "|9.	|Udinese V Empoli           |2022/01/05	|02.45 WIB  |" << endl;
						cout << "|10.	|Inter V Napoli             |2022/01/05	|02.45 WIB  |" << endl;
						cout << "-------------------------------------------------------------" << endl;
					}
					else {
						k = true;
						cout << "Wrong Input" << endl;
					}
					
					//Choose Class
					cout << "What class do you want to choose?" << endl;
					cout << "Class ([E]conomy / [V]IP)	:"; cin >> Class;
					Class = tolower(Class);
					if (Class == 'e') {
						cout << "Your price for this ticket would be" << economy << endl;
					}
					else {
						cout << "Your price for this ticket would be" << VIP << endl;
					}
					
					//Make sure the order
					cout << "Are you sure want to order this ticket? Please make sure your data!" << endl;
					cout << "Name" << name << endl;
					cout << "Gender" << gender << endl;
					cout << "League" << league << endl;
				}
			}
			else if (order == 'n') {
				i = false;
				cout << "Have a great day, hope you have enough money later" << endl;
			}
			else {
				i = true;
				cout << "Please enter the right input" << endl;
			}
		}
		cout << "Do you want to order the ticket again? (y/n)"; cin >> again; system ("cls");	
	}while(again == 'y' || again == 'Y');
		cout << "Thank you to order the ticket" << endl;
		
	return 0;
}
