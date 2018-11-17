# BringinTextFile
Input Information from a text file.
#include <iostream>
#include <fstream>
#include <iomanip>
#include <string>

using namespace std;
int main()
{
	bool End_Of_File = false;
	string Info;
	int Number;

	fstream MyFile;
	MyFile.open ("Test.txt", ios::in);

	while (!End_Of_File)
	{

		if (MyFile.eof())
			End_Of_File = true;
		else
		{
			MyFile >> Info;
			MyFile >> Number;
			cout << "\n\t" << setw(15) << left << Info;
			cout << setw(6) << Number;
			cout << endl << endl;
		}

	}

	MyFile.close();
	system("pause");
	return 0;


}
