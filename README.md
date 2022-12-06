#include <iostream>	
#include <string>
#include <ctime>

using namespace std;

int main ()
{
	string name, gender, league, matchLaLiga, dateLaLiga, timeLaLiga, matchPremiere, datePremiere, timePremiere, matchItalia, dateItalia, timeItalia, price;
	string LaLigaStadium[11] = {"", "Montilivi", "Benito Villamarin Stadium", "Wanda Metropolitano", "Alfonso Perez", "Balaidos Stadium", "Estadio Nuevo Mirandilla", "Nuevo Jose Zorrilla Stadium", "Camp Nou", "Anoeta Stadium", "Estadio Ciudad de Valencia"};
	string PremiereStadium[11] = {"", "Gtech Community Stadium", "st. Mary's stadium", "King Power stadium", "Selhurst Park stadium", "Goodison Park","Villa Park", "Emirates stadium", "stamford bridge", "Old Trafford","Elland Road"};
	string ItaliaStadium[11] = {"", "Stadio Arechi", "Stadio citta del tricola", "Olimpico di Torino", "Alberto Picco", "Stadio Olimpico", "Stadio Comunale Via del Mare", "Stadio Artemio Franchi", "Giovanni Zini Stadium", "Friuli", "San Siro"};
	char  genderChoose, again, order;
	char chooseEconomy;
	char chooseVIP;
	char ticketClass;
	char Class;
	int chooseLeague;
	int chooseLaLigaMatch = 0;
	int choosePremiereMatch =0;
	int chooseItaliaMatch = 0;
	
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
					system ("cls"); 
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
					} 
				}
				
				//Choose League
				bool k = true;
				while (k) {
					cout << "Please select the league : " << endl;
					cout << "------------------------" << endl;
					cout << "|No. | League          |" << endl;
					cout << "------------------------" << endl;
					cout << "|1.  | La Liga         |" << endl;
					cout << "|2.  | Premier League  |" << endl;
					cout << "|3.  | Serie A Italia  |" << endl;
					cout << "------------------------" << endl;
					cout << "Input your choice [1/2/3] = "; cin >> chooseLeague;
					cout << endl;
					system ("cls");
					
					//Choose Match
					if (chooseLeague == 1){
						k = false;
						league = "La Liga";
						bool l = true;
						while (l){
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
							cout << "\n" << "Please Choose the match that you want to see" << endl;
							cin >> chooseLaLigaMatch;
							system ("cls");
							
							if (chooseLaLigaMatch == 1) {
								l = false;
								matchLaLiga = "Betis V Rayo";
								dateLaLiga = "2022/12/30";
								timeLaLiga = "23.00 WIB";
							}
							else if (chooseLaLigaMatch == 2) {
								l = false;
								matchLaLiga = "Girona V Rayo";
								dateLaLiga = "2022/12/29";
								timeLaLiga = "01.15 WIB";
							}
							else if (chooseLaLigaMatch == 3) {
								l = false;
								matchLaLiga = "Atletico Madrid V Elche";
								dateLaLiga = "2022/12/30";
								timeLaLiga = "03.30 WIB";
							}
							else if (chooseLaLigaMatch == 4) {
								l = false;
								matchLaLiga = "Getafe V Mallorca";
								dateLaLiga = "2022/12/30";
								timeLaLiga = "23.00 WIB";
							}
							else if (chooseLaLigaMatch == 5) {
								l = false;
								matchLaLiga = "Celta V Sevilla";
								dateLaLiga = "2022/12/31";
								timeLaLiga = "01.15 WIB";
							}
							else if (chooseLaLigaMatch == 6) {
								l = false;
								matchLaLiga = "Cadiz V Almeria";
								dateLaLiga = "2022/12/31";
								timeLaLiga = "01.15 WIB";
							}
							else if (chooseLaLigaMatch == 7) {
								l = false;
								matchLaLiga = "Valladolid V Madrid";
								dateLaLiga = "2022/12/31";
								timeLaLiga = "03.30 WIB";
							}
							else if (chooseLaLigaMatch == 8) {
								l = false;
								matchLaLiga = "Barcelona V Espanyol";
								dateLaLiga = "2022/12/31";
								timeLaLiga = "20.00 WIB";
							}
							else if (chooseLaLigaMatch == 9) {
								l = false;
								matchLaLiga = "Real Sociedad V Osasuna";
								dateLaLiga = "2022/12/31";
								timeLaLiga = "22.15 WIB";
							}
							else if (chooseLaLigaMatch == 10) {
								l = false;
								matchLaLiga = "Villarreal V Valencia";
								dateLaLiga = "2022/12/31";
								timeLaLiga = "22.15 WIB";
							}
							else {
								l = true;
								cout << "Please input the right input!" << endl;
							}
						}
					}
					else if (chooseLeague == 2){
						k = false;
						league = "Premier League";
						bool m = true;
						while (m){
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
							cout << "\n" << "Please Choose the match that you want to see" << endl;
							cin >> choosePremiereMatch;
							system ("cls");
							
							if (choosePremiereMatch == 1) {
								m = false;
								matchPremiere = "Brentford V Tottenham";
								datePremiere = "2022/12/26";
								timePremiere = "19.30 WIB";
							}
							else if (choosePremiereMatch == 2) {
								m = false;
								matchPremiere = "Southampton V Brighton";
								datePremiere = "2022/12/26";
								timePremiere = "22.00 WIB";
							}
							else if (choosePremiereMatch == 3) {
								m = false;
								matchPremiere = "Leicester V Newcastle ";
								datePremiere = "2022/12/26";
								timePremiere = "22.00 WIB";
							}
							else if (choosePremiereMatch == 4) {
								m = false;
								matchPremiere = "Crystal Palace V Fulham";
								datePremiere = "2022/12/26";
								timePremiere = "22.00 WIB";
							}
							else if (choosePremiereMatch == 5) {
								m = false;
								matchPremiere = "Everton V Wolves ";
								datePremiere = "2022/12/26";
								timePremiere = "22.00 WIB";
							}
							else if (choosePremiereMatch == 6) {
								m = false;
								matchPremiere = "Aston Villa V Liverpoo";
								datePremiere = "2022/12/27";
								timePremiere = "00.30 WIB";
							}
							else if (choosePremiereMatch == 7) {
								m = false;
								matchPremiere = "Arsenal V West Ham ";
								datePremiere = "2022/12/27";
								timePremiere = "03.30 WIB";
							}
							else if (choosePremiereMatch == 8) {
								m = false;
								matchPremiere = "Chelsea V Bournemouth";
								datePremiere = "2022/12/28";
								timePremiere = "00.30 WIB";
							}
							else if (choosePremiereMatch == 9) {
								m = false;
								matchPremiere = "Man Utd V Nottingham";
								datePremiere = "2022/12/28";
								timePremiere = "03.00 WIB";
							}
							else if (choosePremiereMatch == 10) {
								m = false;
								matchPremiere = "Leeds V Man City ";
								datePremiere = "2022/12/29";
								timePremiere = "03.00 WIB";
							}
							else {
								m = true;
								cout << "Please input the right input!" << endl;

							}
						}		
					}
					else if (chooseLeague == 3){
						k = false;
						league = "Serie A Italia";
						bool n = true;
						while (n) {
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
							
							cout << "\n" << "Please Choose the match that you want to see" << endl;
							cin >> chooseItaliaMatch;
							system ("cls");
							
							if (chooseItaliaMatch == 1){
								n = false;
								matchItalia = "Salernitana V Milan";
								dateItalia = "2022/01/04";
								timeItalia = "18.30 WIB";
							}
							else if (chooseItaliaMatch == 2){
								n = false;
								matchItalia = "Sassuolo V Sampdoria";
								dateItalia = "2022/01/04";
								timeItalia = "18.30 WIB";
							}
							else if (chooseItaliaMatch == 3){
								n = false;
								matchItalia = "Torino V Verona n";
								dateItalia = "2022/01/04";
								timeItalia = "20.30 WIB";
							}
							else if (chooseItaliaMatch == 4){
								n = false;
								matchItalia = "Spezia V Atalanta";
								dateItalia = "2022/01/04";
								timeItalia = "22.30 WIB";
							}
							else if (chooseItaliaMatch == 5){
								n = false;
								matchItalia = "Roma V Bologna";
								dateItalia = "2022/01/04";
								timeItalia = "22.30 WIB";
							}
							else if (chooseItaliaMatch == 6){
								n = false;
								matchItalia = "Lecce V Lazio";
								dateItalia = "2022/01/04";
								timeItalia = "00.30 WIB";
							}
							else if (chooseItaliaMatch == 7){
								n = false;
								matchItalia = "Fiorentina V Monza";
								dateItalia = "2022/01/05";
								timeItalia = "00.30 WIB";
							}
							else if (chooseItaliaMatch == 8){
								n = false;
								matchItalia = "Cremonese V Juventus";
								dateItalia = "2022/01/05";
								timeItalia = "00.30 WIB";
							}
								else if (chooseItaliaMatch == 9){
								n = false;
								matchItalia = "Udinese V Empoli";
								dateItalia = "2022/01/05";
								timeItalia = "02.45 WIB";
							}
								else if (chooseItaliaMatch == 10){
								n = false;
								matchItalia = "Inter V Napoli";
								dateItalia = "2022/01/05";
								timeItalia = "02.45 WIB";
							}
							else {
								n = true;
								cout << "Please input the right input!" << endl;
							}
						}
					}
					else {
						k = true;
						cout << "Wrong Input" << endl;
					}	
				}
					
					//Choose Class
					bool q = true;
					// while(q) {
						while (q) {
							
							cout << "What class do you want to choose?" << endl;
							cout << "Class ([E]conomy / [V]IP)	:"; 
							cin >> ticketClass;
							Class = ticketClass;
							system ("cls");
							
							Class = tolower(Class);
							if (Class == 'e') {
								// q = false;
								bool o = true;
								while (o) {
									cout << "Your price for this ticket would be  IDR1.500.000" << endl;
									cout << "Are you sure want to choose economy class? [y/n]" << endl;
									cin >> chooseEconomy; system ("cls");
									chooseEconomy = tolower(chooseEconomy);
									if (chooseEconomy == 'y') {
										price = "1.500.000";
										o = false;
										q = false;
										break;
									}
									else if (chooseEconomy == 'n'){
										o = false;
										// break;
									}
									else {
										// o = true;
										cout << "Please input the right input!" << endl;
									}
									// break;
								}
								// break;
							}
							else if (Class == 'v'){
								// q = false;
								bool p = true;
								while (p) {
									cout << "Your price for this ticket would be  IDR5.000.000" <<  endl;
									cout << "Are you sure want to choose VIP class? [y/n]" << endl;
									cin >> chooseVIP; system ("cls");
									chooseVIP = tolower(chooseVIP);
									if (chooseVIP == 'y') {
										price = "5.000.000";
										p = false;
										q = false;
										break;
									}
									else if (chooseVIP == 'n') {
										p = false;
										// break;
									}
									else {
										p = true;
										cout << "Please input the right input!" << endl;
									}
									// break;
								}
								// break;
							}
							else {
								q = true;
								cout << "Please input the right input!" << endl;
							}
						}
					
					//The Summarry
					cout << "Here are the data of your ticket!" << endl;
					cout << "Name      : " << name << endl;
					cout << "Gender    : " << gender << endl;
					cout << "League    : " << league << endl;
					cout << "Match     : " << matchLaLiga << matchPremiere << matchItalia << endl;
					cout << "Date      : " << dateLaLiga << datePremiere << dateItalia << endl;
					cout << "Time      : " << timeLaLiga << timePremiere << timeItalia << endl;
					cout << "Price     : " << "IDR" << price << endl; 
					cout << "Stadium   : " << LaLigaStadium[chooseLaLigaMatch] << PremiereStadium[choosePremiereMatch] << ItaliaStadium[chooseItaliaMatch] << endl;
					
					time_t currtime = time (0);
					char *mytime = ctime(&currtime);
					cout << "\n" << "Current Date and Time " << endl;
					cout << mytime << endl;
					
					
					cout << "\n" << "Do you want to order the ticket again? (y/n)"; 
					cin >> again; 
					system ("cls");
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
	}while(again == 'y' || again == 'Y');
		cout << "Thank you for using us!" << endl;
		
}
