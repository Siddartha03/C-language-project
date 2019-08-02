# C++-language-project
//Student Scholarship System

#include<iostream>
#include<string.h>
#include<fstream>
using namespace std;
class A
{
	char a[100],b[100],c[100];
	int age;
	public:
		void getdata()
		{
			
			ofstream file;
			file.open("sister.txt",ios::app);
			cout<<endl<<"        Enter Your Name : ";
			cin>>a;
			file<<endl<<"Student Name Is : ";
			file<<a;
			cout<<endl<<"        Enter Your Father Name : ";
			cin>>b;
			file<<endl<<"Student Father Is : ";
			file<<b;
			cout<<endl<<"        Enter Your Mother Name : ";
			cin>>c;
			file<<endl<<"Student Mother Is : ";
			file<<c;
			cout<<endl<<"        Enter Student Age : ";
			cin>>age;
			file<<endl<<"Student Age : ";
			file<<age;
			file.close();
	    }
};
class B:public A
{
	float marks1,marks2,marks3,marks4,fees,scholorship;
	int a,b,c;
	int d=1;
	public:
			
		void put()
		{	
			ofstream file;
			file.open("sister.txt",ios::app);
		  marks1:
		  {
			cout<<endl<<endl<<"        Enter Student Marks percentage in 10th class : ";
				cin>>marks1;	
			if(marks1>100 || marks1<1)
			{
			cout<<endl<<"        User enter wrong percentage please eter the correct percentage in 10th class : ";
		    goto marks1;
		    }
		    file<<endl<<"Student Marks in 10th class : ";
			file<<marks1;
		  }
		  
		  marks2:
		  {
			cout<<endl<<"        Enter Student Marks percentage in 12th class : ";
			cin>>marks2;
				if(marks2>100 || marks2<1)
			{
			cout<<endl<<"        User enter wrong percentage please eter the correct percentage : ";
			goto marks2;
		    }
		    file<<endl<<"Student Marks percentage in 12th class : ";
			file<<marks2;
		  }
		  marks3:
		 {
			cout<<endl<<"        Enter Student Marks percentage in LPUNEST exam outoff 400 marks : ";
			cin>>marks3;
			if(marks3>100 || marks3<1)
			{
				cout<<endl<<"        User enter wrong percentage please enter the correct percentage in LPUNEST : ";
			   goto marks3;
			}
			file<<endl<<"Student Marks percentage in LPUNEST exam : ";
			file<<marks3;
		  }
		  
			if( (marks2<=100 && marks2>=90) || (marks3<=100 && marks3>=90))
			{
			fees=(25*180000)/100;
			cout<<endl<<"Total Fee : 1,80,000 Rs/-"<<endl<<"Scholorship : 75%"<<endl<<"Fee after scholorship : "<<fees<< "Rs/-"<<endl;
		    file<<endl<<"Student Fee List : ";
			file<<"Total Fee : 1,80,000 Rs/-"<<endl<<"Scholorship : 75%"<<endl<<"Fee after scholorship : "<<fees<< "Rs/-"<<endl;
			}else
			
			if( (marks2>=80 && marks2<=89.99999) || (marks3>=80 && marks3<=89.99999) )
			{
			fees=(50*180000)/100;
			cout<<endl<<"Total Fee : 1,80,000 Rs/-"<<endl<<"Scholorship : 50%"<<endl<<"Fee after scholorship : "<<fees<<" Rs/-"<<endl;
		    file<<endl<<"Student Fee List : ";
			file<<"Total Fee : 1,80,000 Rs/-"<<endl<<"Scholorship : 50%"<<endl<<"Fee after scholorship : "<<fees<< "Rs/-"<<endl;
			}else
			
			if( (marks2>=70 && marks2<=79.99999) || (marks3>=70 && marks3<=79.99999) )
			{
			fees=(75*180000)/100;
			cout<<endl<<"Total Fee : 1,80,000 Rs/-"<<endl<<"Scholorship : 25%"<<endl<<"Fee after scholorship : "<<fees<<" Rs/-"<<endl;
	        file<<endl<<"Student Fee List : ";
			file<<"Total Fee : 1,80,000 Rs/-"<<endl<<"Scholorship : 25%"<<endl<<"Fee after scholorship : "<<fees<< "Rs/-"<<endl;
		    }else
			
			if(marks2<70 && marks3<70)
			{
			cout<<endl<<"Student is not eligible for LPU "<<endl;
	        file<<endl<<"Student is not eligible for LPU"<<endl<<endl<<endl<<endl;
			}
			file.close();
	}
	void graduate()
	{
	        ofstream file;
			file.open("sister.txt",ios::app);
		  marks1:
		  {
			cout<<endl<<endl<<"        Enter Student Marks percentage in 10th class : ";
				cin>>marks1;	
			if(marks1>100 || marks1<1)
			{
			cout<<endl<<"        User enter wrong percentage please eter the correct percentage in 10th class : ";
		    goto marks1;
		    }
		    file<<endl<<"Student Marks in 10th class : ";
			file<<marks1;
		  }
		  
		  marks2:
		  {
			cout<<endl<<"        Enter Student Marks percentage in 12th class : ";
			cin>>marks2;
				if(marks2>100 || marks2<1)
			{
			cout<<endl<<"        User enter wrong percentage please eter the correct percentage : ";
			goto marks2;
		    }
		    file<<endl<<"Student Marks percentage in 12th class : ";
			file<<marks2;
		  }
	         
		   marks4:
		 {
			cout<<endl<<"        Enter Student Marks percentage in Graduation : ";
			cin>>marks4;
			if(marks4>100 || marks4<1)
			{
				cout<<endl<<"        User enter wrong percentage please enter the correct percentage in Graduation : ";
			   goto marks4;
			}
			file<<endl<<"Student Marks percentage in Graduation : ";
			file<<marks4;
		  }
		  
		  if(marks4>=90 && marks4<=100)
		  {
		    fees=(25*240000)/100;
			cout<<endl<<"Total Fee : 2,40,000 Rs/-"<<endl<<"Scholorship : 75%"<<endl<<"Fee after scholorship : "<<fees<< "Rs/-"<<endl;
		    file<<endl<<"Student Fee List : ";
			file<<"Total Fee : 2,40,000 Rs/-"<<endl<<"Scholorship : 75%"<<endl<<"Fee after scholorship : "<<fees<< "Rs/-"<<endl;
			}else
		
		   if(marks4>=80 && marks4<=89.99999)
			{
			fees=(50*180000)/100;
			cout<<endl<<"Total Fee : 2,40,000 Rs/-"<<endl<<"Scholorship : 50%"<<endl<<"Fee after scholorship : "<<fees<<" Rs/-"<<endl;
		    file<<endl<<"Student Fee List : ";
			file<<"Total Fee : 2,40,000 Rs/-"<<endl<<"Scholorship : 50%"<<endl<<"Fee after scholorship : "<<fees<< "Rs/-"<<endl;
			}else
				
			if(marks4>=70 && marks4<=79.99999)
			{
			fees=(75*180000)/100;
			cout<<endl<<"Total Fee : 2,40,000 Rs/-"<<endl<<"Scholorship : 20%"<<endl<<"Fee after scholorship : "<<fees<<" Rs/-"<<endl;
		    file<<endl<<"Student Fee List : ";
			file<<"Total Fee : 2,40,000 Rs/-"<<endl<<"Scholorship : 20%"<<endl<<"Fee after scholorship : "<<fees<< "Rs/-"<<endl;
			}else
			
			if(marks4<70)
			{
			cout<<endl<<"Student is not eligible for LPU "<<endl<<endl<<endl;
	        file<<endl<<"Student is not eligible for LPU"<<endl<<endl<<endl<<endl<<endl<<endl;
			}
			file.close();	
	}
 
    void goku()
    {  
	    cout<<"                                  SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	cout<<"                             -----------------------------------------------------"<<endl<<endl;
	cout<<"Choose following :"<<endl;
	cout<<endl<<"1. After 10th class"<<endl<<"2. After 12th class"<<endl<<"3. After Graduation"<<endl<<"4. Lateral Entry"<<endl;
	cin>>a;
	 system("CLS");
	switch(a)
	{
		case 1:
				cout<<"                                     SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	        cout<<"                               -----------------------------------------------------"<<endl<<endl;
			cout<<"1. Engineering"<<endl<<"2. Management Courses"<<endl<<"3. Mass Communication Coures"<<endl<<"4. Medical Courses"<<endl<<"5. Multimedia, Animation and Gaming Courses"<<endl<<"6. fashion and Interior Designing Courses"<<endl;
            cout<<endl<<"Enter your choice : ";
		 cin>>b; 
		 system("CLS");  
	     switch(b)
		{  case 1:
				cout<<"                                     SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	        cout<<"                                -----------------------------------------------------"<<endl<<endl;
			cout<<"Student choose 'Engineering' "<<endl;
			cout<<"Which course you want in the following options : "<<endl<<endl;
		  	cout<<"1. B.Tech.(Computer Science & Technology)"<<endl<<"2. B.Sc.(Nanotechnology)"<<endl<<"3. B.Tech.(Biotechnology)"<<"4. B.Tech.(Civil Engineering)"<<endl<<"5. B.Tech.(Mechanical Engineering)"<<endl;
		    cout<<endl<<"Enter your choice : ";
		 cin>>c;
		  system("CLS");
		 switch(c)
		 {
		 	case 1:
		 		cout<<"                                    SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                              -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'CSE' "<<endl;
		  	getdata();
		  	put();
		  	 break;
		  	
		    case 2:
		    	cout<<"                                    SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                              -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Nanotechnology' "<<endl;
		  	getdata();
		  	put();
		  	 break;
			   	
		    case 3:
		    	cout<<"                                    SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                              -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Biotechnology' "<<endl;
		  	getdata();
		  	put();
			 break;
			  
			case 4:
				cout<<"                                     SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                              -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Civil Engineering' "<<endl;
		    getdata();
		  	put();
			  break;
			  	  
			case 5:
				cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Mechanical Engineering' "<<endl;
		  	getdata();
		  	put();
			  break;
		 }break;
		 
		   case 2:
		   		cout<<"                              SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                        -----------------------------------------------------"<<endl<<endl;
		   	cout<<"Student choose 'Management Courses' "<<endl;
		   	cout<<"Which course you want in the following options : "<<endl<<endl;
		   	cout<<"1. B.B.A."<<endl<<"2. Bachelor of Hotel Managemenet & Catering Technology "<<endl<<"3. B.Sc. (Airlines, Tourism & Hospital Management) "<<endl<<"4. B.Sc. (Hotel Management) "<<endl;
		  	 cout<<endl<<"Enter your choice : ";
			   cin>>c;
		  	  system("CLS");
		 switch(c)
		 {
		 	case 1:
		 		cout<<"                                SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                         -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.B.A.' "<<endl;
		  	getdata();
		    put();
		  	 break;
		  	
		    case 2:
		    	cout<<"                                SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                          -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Bachelor of Hotel Managemenet & Catering Technology' "<<endl;
		  	getdata();
		  	put();
		  	 break;
			   	
		    case 3:
		    	cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Sc. (Airlines, Tourism & Hospital Management)' "<<endl;
		  	getdata();
		  	put();
			 break;
			  
			case 4:
					cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Sc. (Hotel Management)' "<<endl;
		  	getdata();
		  	put();
			  break;
			  	  
			case 5:
					cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Mechanical Engineering' "<<endl;
		  	getdata();
		  	put();
			  break;	
		 }break;
		 
		  	case 3:
		  			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  		cout<<"Student choose 'Mass Communication Courses' "<<endl;
		  		cout<<"MJMC (Journalism & Mas Communication) "<<endl;
		  		getdata();
		  		put();
		  		break;
		  		
		  	case 4:	
			    cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
            	cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  		
		  			cout<<"Student choose 'Medical Courses' "<<endl;
		  			cout<<"Which course you want in the following options : "<<endl<<endl;
					cout<<"1. B.P.T"<<endl<<"2. B.Pharms"<<endl<<"3. Bachelor of Ayurvedic Pharmacy"<<endl<<"4. M.P.T.(Cardio Pulmonary Physiotherapy)"<<endl<<"5. M.P.T(Neurology)"<<endl;
			        cout<<endl<<"Enter your choice : ";
			cin>>c;
			system("CLS");
		 switch(c)
		 {
		 	case 1:
		 			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose ' B.P.T' "<<endl;
		  	getdata();
		  	put();
		  	 break;
		  	
		    case 2:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Pharms' "<<endl;
		  	getdata();
		  	put();
		  	 break;
			   	
		    case 3:
		  	cout<<"Student choose 'Bachelor of Ayurvedic Pharmacy' "<<endl;
		  	getdata();
		  	put();
			 break;
			  
			case 4:
		  	cout<<"Student choose 'M.P.T.(Cardio Pulmonary Physiotherapy)' "<<endl;
		  	getdata();
		  	put();
			  break;
			  	  
			case 5:
		  	cout<<"Student choose 'M.P.T(Neurology)' "<<endl;
		  	getdata();
		  	put();
			  break;	
		 }break;
		 
		 case 5:
		 		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		 	cout<<"Student choose 'Multimedia, Animation and Gaming Courses' "<<endl;
		 	cout<<"Which course you want in the following options : "<<endl<<endl;
		 	cout<<"1. B.Design (Animation)"<<endl<<"2. B.Design (Graphics) "<<endl<<"3. B.Design (Animation) + M.Design "<<endl;
		    cout<<endl<<"Enter your choice : ";
		cin>>c;
		 system("CLS");
	    switch(c)
		 {
		 	case 1:
		 			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose ' B.Design (Animation) ' "<<endl;
		  	getdata();
		  	put();
		  	 break;
		  	
		    case 2:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Design (Graphics)' "<<endl;
		  	getdata();
		  	put();
		  	 break;
			   	
		    case 3:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Design (Animation) + M.Design' "<<endl;
		  	getdata();
		  	put();
			 break;
        }break;
        
        case 6:
        		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		 	cout<<"Student choose 'fashion and Interior Designing Courses' "<<endl;
		 	cout<<"Which course you want in the following options : "<<endl<<endl;
		 	cout<<"1. B.Des. (Interior Design)"<<endl<<"2. B.Sc. (Fashion Design)"<<endl<<"3. B.Sc. (Fashion Technology)"<<endl<<"4. B.Sc. (Interior Design)"<<endl;
		    cout<<endl<<"Enter your choice : ";
		    cin>>c;
		     system("CLS");
		 switch(c)
		 {
		 	case 1:
		 			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Des. (Interior Design) ' "<<endl;
		  	getdata();
		  	put();
		  	 break;
		  	
		    case 2:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Sc. (Fashion Design)' "<<endl;
		  	getdata();
		  	put();
		  	 break;
			   	
		    case 3:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Sc. (Fashion Technology)' "<<endl;
		  	getdata();
		  	put();
			 break;
			  
			case 4:
					cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Sc. (Interior Design)' "<<endl;
		  	getdata();
		  	put();break;
		}break;
		
      }break;
      
      	case 2:
      			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
			cout<<"1. Engineering"<<endl<<"2. Management Courses"<<endl<<"3. Mass Communication Coures"<<endl<<"4. Medical Courses"<<endl<<"5. Multimedia, Animation and Gaming Courses"<<endl<<"6. fashion and Interior Designing Courses"<<endl;
         cin>>b;
		  system("CLS");   
	     switch(b)
		{  case 1:
				cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
			cout<<"Student choose 'Engineering' "<<endl;
			cout<<"Which course you want in the following options : "<<endl<<endl;
		  	cout<<"1. B.Tech.(Computer Science & Technology)"<<endl<<"2. B.Sc.(Nanotechnology)"<<endl<<"3. B.Tech.(Biotechnology)"<<"4. B.Tech.(Civil Engineering)"<<endl<<"5. B.Tech.(Mechanical Engineering)"<<endl;
		    cout<<endl<<"Enter your choice : ";
		 cin>>c;
		  system("CLS");
		 switch(c)
		 {
		 	case 1:
		 			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'CSE' "<<endl;
		  	getdata();
		  	put();
		  	 break;
		  	
		    case 2:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Nanotechnology' "<<endl;
		  	getdata();
		  	put();
		  	 break;
			   	
		    case 3:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Biotechnology' "<<endl;
		  	getdata();
		  	put();
			 break;
			  
			case 4:
					cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Civil Engineering' "<<endl;
		  	getdata();
		  	put();
			  break;
			  	  
			case 5:
					cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Mechanical Engineering' "<<endl;
		  	getdata();
		  	put();
			  break;	
		 }break;
		 
		   case 2:
		   		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		   	cout<<"Student choose 'Management Courses' "<<endl;
		   	cout<<"Which course you want in the following options : "<<endl<<endl;
		   	cout<<"1. B.B.A."<<endl<<"2. Bachelor of Hotel Managemenet & Catering Technology "<<endl<<"3. B.Sc. (Airlines, Tourism & Hospital Management) "<<endl<<"4. B.Sc. (Hotel Management) "<<endl;
		  	cout<<endl<<"Enter your choice : "; 
			   cin>>c;
		  	  system("CLS");
		 switch(c)
		 {
		 	case 1:
		 			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.B.A.' "<<endl;
		  	getdata();
		  	put();
		  	 break;
		  	
		    case 2:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Bachelor of Hotel Managemenet & Catering Technology' "<<endl;
		  	getdata();
		  	put();
		  	 break;
			   	
		    case 3:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Sc. (Airlines, Tourism & Hospital Management)' "<<endl;
		  	getdata();
		  	put();
			 break;
			  
			case 4:
					cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Sc. (Hotel Management)' "<<endl;
		  	getdata();
		  	put();
			  break;
			  	  
			case 5:
					cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Mechanical Engineering' "<<endl;
		  	getdata();
		  	put();
			  break;
			  	
		 }break;
		  	case 3:
		  			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  		cout<<"Student choose 'Mass Communication Courses' "<<endl;
		  		cout<<"MJMC (Journalism & Mas Communication) "<<endl;
		  		getdata();
		  		put();
		  		break;
		  		
		  	case 4:
		  			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	            cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  			cout<<"Student choose 'Medical Courses' "<<endl;
		  			cout<<"Which course you want in the following options : "<<endl<<endl;
					cout<<"1. B.P.T"<<endl<<"2. B.Pharms"<<endl<<"3. Bachelor of Ayurvedic Pharmacy"<<endl<<"4. M.P.T.(Cardio Pulmonary Physiotherapy)"<<endl<<"5. M.P.T(Neurology)"<<endl;
			   cout<<endl<<"Enter your choice : ";
			cin>>c;
			 system("CLS");
		 switch(c)
		 {
		 	case 1:
		 			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose ' B.P.T' "<<endl;
		  	getdata();
		  	put();
		  	 break;
		  	
		    case 2:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Pharms' "<<endl;
		  	getdata();
		  	put();
		  	 break;
			   	
		    case 3:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Bachelor of Ayurvedic Pharmacy' "<<endl;
		  	getdata();
		  	put();
			 break;
			  
			case 4:
					cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'M.P.T.(Cardio Pulmonary Physiotherapy)' "<<endl;
		  	getdata();
		  	put();
			  break;
			  	  
			case 5:
					cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'M.P.T(Neurology)' "<<endl;
		  	getdata();
		  	put();
			  break;	
		 }break;
		 
		 case 5:
		 		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		 	cout<<"Student choose 'Multimedia, Animation and Gaming Courses' "<<endl;
		 	cout<<"Which course you want in the following options : "<<endl<<endl;
		  	cout<<"1. B.Design (Animation)"<<endl<<"2. B.Design (Graphics) "<<endl<<"3. B.Design (Animation) + M.Design "<<endl;
		  cout<<endl<<"Enter your choice : ";
		cin>>c;
		 system("CLS");
	    switch(c)
		 {
		 	case 1:
		 			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose ' B.Design (Animation) ' "<<endl;
		  	getdata();
		  	put();
		  	 break;
		  	
		    case 2:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Design (Graphics)' "<<endl;
		  	getdata();
		  	put();
		  	 break;
			   	
		    case 3:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Design (Animation) + M.Design' "<<endl;
		  	getdata();
		  	put();
			 break;
        }break;
        
        case 6:
        		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		 	cout<<"Student choose 'fashion and Interior Designing Courses' "<<endl;
		 	cout<<"Which course you want in the following options : "<<endl<<endl;
		 	cout<<"1. B.Des. (Interior Design)"<<endl<<"2. B.Sc. (Fashion Design)"<<endl<<"3. B.Sc. (Fashion Technology)"<<endl<<"4. B.Sc. (Interior Design)"<<endl;
		    cout<<endl<<"Enter your choice : ";
			cin>>c;
		     system("CLS");
		 switch(c)
		 {
		 	case 1:
		 			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Des. (Interior Design) ' "<<endl;
		  	getdata();
		  	put();
		  	 break;
		  	
		    case 2:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Sc. (Fashion Design)' "<<endl;
		  	getdata();
		  	put();
		  	 break;
			   	
		    case 3:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Sc. (Fashion Technology)' "<<endl;
		  	getdata();
		  	put();
			 break;
			  
			case 4:
					cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose ' B.Sc. (Interior Design)' "<<endl;
		  	getdata();
		  	put();
			  break;
		}break;
		
      }break;
  
       case 3:
       		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	    cout<<"                     -----------------------------------------------------"<<endl<<endl;
	   cout<<"1. Engineering"<<endl<<"2. management"<<endl<<"3. Computer Applications and IT"<<endl<<"4. Commerce"<<endl<<"5. Law"<<endl<<"6. Agriculture"<<endl;
	    cout<<endl<<"Enter your choice : ";
		cin>>b;
		 system("CLS");   
	     switch(b)
		{  case 1:
				cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
			cout<<"Student choose 'Engineering' "<<endl;
			cout<<"Which course you want in the following options : "<<endl<<endl;
			cout<<"1. M.Tech. (VLSI Design)"<<endl<<"2. M.Tech. (Manufacturing Engineering)"<<endl<<"3. M.Tech. (Thermal Engineering)"<<endl<<"4. M.Tech. (Robotics)"<<endl;
		cout<<endl<<"Enter your choice : ";
		cin>>c;
		system("CLS");
		 switch(c)
		 {
		 	case 1:
		 			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'M.Tech. (VLSI Design)' "<<endl;
		  	getdata();
		  	graduate();
		  	 break;
		  	
		    case 2:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose ' M.Tech. (Manufacturing Engineering)' "<<endl;
		  	getdata();
		  	graduate();
		  	 break;
			   	
		    case 3:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'M.Tech. (Thermal Engineering)' "<<endl;
		  	getdata();
		  	graduate();
			 break;
			  
			case 4:
					cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'M.Tech. (Robotics)' "<<endl;
		    getdata();
		  	graduate();
			  break;
		
		 }break;
		 
		   case 2:
		   		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		   	cout<<"Student choose 'management' "<<endl;
		   	cout<<"Which course you want in the following options : "<<endl<<endl;
		   	cout<<"1. MBA (Tourism & Hospitality)"<<endl<<"2. MBA (Hospital & Health Management)"<<endl<<"3. MBA (Information Technology)"<<endl<<"4. International Business"<<endl;
		cout<<endl<<"Enter your choice : ";
		 cin>>c;
		  system("CLS");
		 switch(c)
		 {
		 	case 1:
		 			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose ' MBA (Tourism & Hospitality)' "<<endl;
		  	getdata();
		  	graduate();
		  	 break;
		  	
		    case 2:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'MBA (Hospital & Health Management)' "<<endl;
		  	getdata();
		  	graduate();
		  	 break;
			   	
		    case 3:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'MBA (Information Technology)' "<<endl;
		  	getdata();
		  	graduate();
			 break;
			  
			case 4:
					cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose ' International Business' "<<endl;
		  	getdata();
		  	graduate();
			  break;
		}break;
		
		case 3:
				cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
			cout<<"Student choose 'Computer Applications and IT' "<<endl;
		   	cout<<"Which course you want in the following options : "<<endl<<endl;
		    cout<<"1. MCA"<<endl<<"2. MCA (HONS.)"<<endl;
			cout<<endl<<"Enter your choice : ";
			 cin>>c;
			  system("CLS");
		 switch(c)
		 {
		 	case 1:
		 			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'MCA' "<<endl;
		  	getdata();
		  	graduate();
		  	 break;
		  	
		    case 2:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'MCA (HONS.)' "<<endl;
		  	getdata();
		  	graduate();
		  	 break; 	
		
        }break;
        
        case 4:
        		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		   	cout<<"Student choose 'Commerse' "<<endl;
		   	cout<<"Which course you want in the following options : "<<endl<<endl;
		   	cout<<"1. M.Com."<<endl;
		   	getdata();
		   	graduate();
		   	break;
		   	
		    case 5:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	            cout<<"                     -----------------------------------------------------"<<endl<<endl;
		   	cout<<"Student choose 'Law' "<<endl;
		   	cout<<"Which course you want in the following options : "<<endl<<endl;	
	        cout<<"1. LL.B."<<endl<<"2. LL.M."<<endl;
	       cout<<endl<<"Enter your choice : ";
		 cin>>c;
	     system("CLS");
	     
		 switch(c)
		 {
		 	case 1:
		 			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'LL.B.' "<<endl;
		  	getdata();
		  	graduate();
		  	 break;
		  	
		    case 2:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'LL.M.' "<<endl;
		  	getdata();
		  	graduate();
		  	 break; 	
		
        }break;
        
        case 6:
		  	cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	    cout<<"                     -----------------------------------------------------"<<endl<<endl;
		   	cout<<"Student choose 'Agriculture' "<<endl;
		   	cout<<"Which course you want in the following options : "<<endl<<endl;
            cout<<"1. M.Sc.Ag. (Agronomy)"<<endl<<"2. M.Sc.Ag. (Genetics & Plant Breeding)"<<endl<<"3. M.Sc.Ag. (Soil Science & Agriculture Chemistry)"<<endl<<"4. M.Sc.Ag. (Plant Pathology)"<<endl;
		  cout<<endl<<"Enter your choice : ";
		 cin>>c;
		  system("CLS");
		 switch(c)
		 {
		 	case 1:
		 			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'M.Sc.Ag. (Agronomy)' "<<endl;
		  	getdata();
		  	graduate();
		  	 break;
		  	
		    case 2:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'M.Sc.Ag. (Genetics & Plant Breeding)' "<<endl;
		  	getdata();
		  	graduate();
		  	 break;
			   	
		    case 3:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'M.Sc.Ag. (Soil Science & Agriculture Chemistry)' "<<endl;
		  	getdata();
		  	graduate();
			 break;
			  
			case 4:
					cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'M.Sc.Ag. (Plant Pathology)"<<endl;
		  	getdata();
		  	graduate();
			  break;
		}break;		 
	 }break;
	 
	 case 4:
	 		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	    cout<<"                     -----------------------------------------------------"<<endl<<endl;
			cout<<"1. Engineering"<<endl<<"2. Management Courses"<<endl<<"3. Mass Communication Coures"<<endl<<"4. Medical Courses"<<endl<<"5. Multimedia, Animation and Gaming Courses"<<endl<<"6. fashion and Interior Designing Courses"<<endl;
           cout<<endl<<"Enter your choice : ";
		 cin>>b;
		  system("CLS");   
	     switch(b)
		{  case 1:
				cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
			cout<<"Student choose 'Engineering' "<<endl;
			cout<<"Which course you want in the following options : "<<endl<<endl;
		  	cout<<"1. B.Tech.(Computer Science & Technology)"<<endl<<"2. B.Sc.(Nanotechnology)"<<endl<<"3. B.Tech.(Biotechnology)"<<"4. B.Tech.(Civil Engineering)"<<endl<<"5. B.Tech.(Mechanical Engineering)"<<endl;
		  cout<<endl<<"Enter your choice : ";
		 cin>>c;
		  system("CLS");
		 switch(c)
		 {
		 	case 1:
		 			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'CSE' "<<endl;
		  	getdata();
		  	put();
		  	 break;
		  	
		    case 2:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Nanotechnology' "<<endl;
		  	getdata();
		  	put();
		  	 break;
			   	
		    case 3:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Biotechnology' "<<endl;
		  	getdata();
		  	put();
			 break;
			  
			case 4:
		  	cout<<"Student choose 'Civil Engineering' "<<endl;
		    getdata();
		  	put();
			  break;
			  	  
			case 5:
					cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Mechanical Engineering' "<<endl;
		  	getdata();
		  	put();
			  break;	
		 }break;
		 
		   case 2:
		   		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		   	cout<<"Student choose 'Management Courses' "<<endl;
		   	cout<<"Which course you want in the following options : "<<endl<<endl;
		   	cout<<"1. B.B.A."<<endl<<"2. Bachelor of Hotel Managemenet & Catering Technology "<<endl<<"3. B.Sc. (Airlines, Tourism & Hospital Management) "<<endl<<"4. B.Sc. (Hotel Management) "<<endl;
		  	cout<<endl<<"Enter your choice : ";
			   cin>>c;
		  	  system("CLS");
		 switch(c)
		 {
		 	case 1:
		 			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.B.A.' "<<endl;
		  	getdata();
		    put();
		  	 break;
		  	
		    case 2:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Bachelor of Hotel Managemenet & Catering Technology' "<<endl;
		  	getdata();
		  	put();
		  	 break;
			   	
		    case 3:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Sc. (Airlines, Tourism & Hospital Management)' "<<endl;
		  	getdata();
		  	put();
			 break;
			  
			case 4:
					cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Sc. (Hotel Management)' "<<endl;
		  	getdata();
		  	put();
			  break;
			  	  
			case 5:
					cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Mechanical Engineering' "<<endl;
		  	getdata();
		  	put();
			  break;	
		 }break;
		 
		  	case 3:
		  			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  		cout<<"Student choose 'Mass Communication Courses' "<<endl;
		  		cout<<"MJMC (Journalism & Mas Communication) "<<endl;
		  		getdata();
		  		put();
		  		break;
		  		
		  	case 4:
		  			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	            cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  			cout<<"Student choose 'Medical Courses' "<<endl;
		  			cout<<"Which course you want in the following options : "<<endl<<endl;
					cout<<"1. B.P.T"<<endl<<"2. B.Pharms"<<endl<<"3. Bachelor of Ayurvedic Pharmacy"<<endl<<"4. M.P.T.(Cardio Pulmonary Physiotherapy)"<<endl<<"5. M.P.T(Neurology)"<<endl;
			    cout<<endl<<"Enter your choice : ";
			cin>>c;
			 system("CLS");
		 switch(c)
		 {
		 	case 1:
		 			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose ' B.P.T' "<<endl;
		  	getdata();
		  	put();
		  	 break;
		  	
		    case 2:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Pharms' "<<endl;
		  	getdata();
		  	put();
		  	 break;
			   	
		    case 3:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'Bachelor of Ayurvedic Pharmacy' "<<endl;
		  	getdata();
		  	put();
			 break;
			  
			case 4:
					cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'M.P.T.(Cardio Pulmonary Physiotherapy)' "<<endl;
		  	getdata();
		  	put();
			  break;
			  	  
			case 5:
		  	cout<<"Student choose 'M.P.T(Neurology)' "<<endl;
		  	getdata();
		  	put();
			  break;	
		 }break;
		 
		 case 5:
		 		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		 	cout<<"Student choose 'Multimedia, Animation and Gaming Courses' "<<endl;
		 	cout<<"Which course you want in the following options : "<<endl<<endl;
		 	cout<<"1. B.Design (Animation)"<<endl<<"2. B.Design (Graphics) "<<endl<<"3. B.Design (Animation) + M.Design "<<endl;
		   cout<<endl<<"Enter your choice : ";
		cin>>c;
		 system("CLS");
	    switch(c)
		 {
		 	case 1:
		 			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose ' B.Design (Animation) ' "<<endl;
		  	getdata();
		  	put();
		  	 break;
		  	
		    case 2:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Design (Graphics)' "<<endl;
		  	getdata();
		  	put();
		  	 break;
			   	
		    case 3:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Design (Animation) + M.Design' "<<endl;
		  	getdata();
		  	put();
			 break;
        }break;
        
        case 6:
        		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
    	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		 	cout<<"Student choose 'fashion and Interior Designing Courses' "<<endl;
		 	cout<<"Which course you want in the following options : "<<endl<<endl;
		 	cout<<"1. B.Des. (Interior Design)"<<endl<<"2. B.Sc. (Fashion Design)"<<endl<<"3. B.Sc. (Fashion Technology)"<<endl<<"4. B.Sc. (Interior Design)"<<endl;
		    cout<<endl<<"Enter your choice : ";
			cin>>c;
		     system("CLS");
		 switch(c)
		 {
		 	case 1:
		 			cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Des. (Interior Design) ' "<<endl;
		  	getdata();
		  	put();
		  	 break;
		  	
		    case 2:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Sc. (Fashion Design)' "<<endl;
		  	getdata();
		  	put();
		  	 break;
			   	
		    case 3:
		    		cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Sc. (Fashion Technology)' "<<endl;
		  	getdata();
		  	put();
			 break;
			  
			case 4:
					cout<<"                           SCHOLORSHIP CALCULATOR FOR FRESH ADMISSION"<<endl;
       	        cout<<"                     -----------------------------------------------------"<<endl<<endl;
		  	cout<<"Student choose 'B.Sc. (Interior Design)' "<<endl;
		  	getdata();
		  	put();break;
		}break;
		
      }break;
   }
  cout<<endl<<"For New Entry press '1'"<<endl;
  cin>>d;
   system("CLS");
  if(d==1)
  goku(); 
      else
   exit(0);

   }
 
 };
main()
{   
	system("color A");
  B obj;
  obj.goku();	
}
