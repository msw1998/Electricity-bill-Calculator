#include <iostream>
using namespace std;
void residential()
    {
        int units,tvl = 35, bank_charges = 8, fixed_charges;
        float surcharge, amount, meter_rent = 15.0, electricity_duty, total_amount, GST,GST2,GST_retailers,load;
        char type;
        cout<<"Enter the units consumed: ";
        cin>>units;
        if(units >+ 1 && units <= 100 )
        {
            amount = units * 5.79;
            surcharge = 0;
        }

        else if (units >100 && units <= 200)
        {
            amount = (100*5.79) + ((units-100)*8.11);
            surcharge = 0;
        }
        else if (units> 200 && units<=300)
        {
            amount = (200*8.11) + ((units-200)* 10.20);
            surcharge = 0;
        }
        else if(units >300 && units <= 700)
        {
            amount = (300* 10.20) + ((units-300)* 15.45);
            surcharge = (units- 300) * 0.55;
        }
        else
        {
            amount = (700*15.45) + ((units - 700)* 17.33);
            surcharge = (700*0.55) + ((units- 700) * 0.67);
        }
        fixed_charges = 0;
        meter_rent = 15.0;
        electricity_duty = 0.015*(amount + surcharge);
        GST = 0.17 * (amount+surcharge+ meter_rent + electricity_duty );
        GST2 = 0;
        GST_retailers = 0;
        total_amount = amount+surcharge+ meter_rent + electricity_duty + GST+GST2 +GST_retailers+ tvl + bank_charges ;
        cout<<"FIxed charges: "<<fixed_charges<<endl;
        cout<<"Variable charges: "<<amount<<endl;
        cout<<"Surcharge: "<<surcharge;
        cout<<"\nMeter Rent: "<<meter_rent;
        cout<<"\nElectricty Duty: "<<electricity_duty;
        cout<<"\nGeneral Sales Tax: "<<GST<<endl;
        cout<<"2% Further GST: "<<GST2;
        cout<<"\nGST on retailers: "<<GST_retailers;
        cout<<"\nTV license fees: "<<tvl;
        cout<<"\nBank charges: "<<bank_charges<<endl;
        cout<<"The total amount billed is: "<<total_amount<<"Rs";
    }
void commercial()
    {
        int units,tvl = 35, bank_charges = 8, fixed_charges;
        float surcharge, amount, meter_rent = 15.0, electricity_duty, total_amount, GST,GST2,GST_retailers,load;
        char type;
        cout<<"Enter you billing type, press L for sanctioned load, P for peak hours:  ";
        cin>>type;
        if(type == 'L')
        {
            cout<<"Enter your sanctioned load in kwh: ";
            cin>>load;
            if(load < 5)
            {
                cout<<"Enter the units billed: ";
                cin>>units;
                fixed_charges = 0;
                amount = units * 17.83;
                surcharge = units * 0.17;
            }
            else
            {
                fixed_charges = 400;
                cout<<"Enter the units billed: ";
                cin>>units;
                amount = units * 15.03;
                surcharge = units * 0.97;
            }

        }
        else if(type == 'P')
        {
            int units1,units2;
            fixed_charges = 400;
            cout<<"Enter number of units during peak hours: ";
            cin>>units1;
            cout<<"Enter number of units during off-peak hours: ";
            cin>>units2;
            surcharge = 0;
            amount = (units1 * 18.00) + (units2 * 12.50 ) ;
        }
        meter_rent = 15.0;
        tvl = 60;
        electricity_duty = 0.02*(amount + surcharge);
        GST = 0.17 * (amount+surcharge+ meter_rent + electricity_duty );
        GST2 = 0.02 * (amount+surcharge+ meter_rent + electricity_duty);
        GST_retailers = 0.05 * (amount+surcharge+ meter_rent + electricity_duty);
        total_amount = amount+surcharge+ meter_rent + electricity_duty + GST +GST2 +GST_retailers+tvl+ bank_charges ;
        cout<<"FIxed charges: "<<fixed_charges<<endl;
        cout<<"Variable charges: "<<amount<<endl;
        cout<<"Surcharge: "<<surcharge;
        cout<<"\nMeter Rent: "<<meter_rent;
        cout<<"\nElectricty Duty: "<<electricity_duty;
        cout<<"\nGeneral Sales Tax: "<<GST<<endl;
        cout<<"2% Further GST: "<<GST2;
        cout<<"\nGST on retailers: "<<GST_retailers;
        cout<<"\nTV license fees: "<<tvl;
        cout<<"\nBank charges: "<<bank_charges<<endl;
        cout<<"The total amount billed is: "<<total_amount<<"Rs";
    }
void industrial()
    {
        int units,tvl = 35, bank_charges = 8, fixed_charges,val,choice , units1,units2;
        float surcharge, amount, meter_rent = 15.0, electricity_duty, total_amount, GST,GST2,GST_retailers,load;
        char type;

        cout<<"Press 1 for load based calculation or Press 2 for time based calculation: ";
        cin>>choice;
        if(choice == 1)
        {
            cout<<"Please Select your category: \nFor Less than 5 kW(at 400/230 V) press 1.\nfor 5-500kW(at 400V) press 2. \nFor all loads upto 5000kW(at 11,33kV) press 3. \nFor all loads upto 5000kW(at 66,132kV) press 4\n";
            cin>>val;
            cout<<"Enter the units consumed: ";
            cin>>units;
            if (val == 1)
            {
                fixed_charges = 0;
                amount = units *14.33;
                surcharge = units *0.17;
            }
            else if (val == 2)
            {
                fixed_charges = 400;
                amount = units * 12.93;
                surcharge = units * 1.07;
            }
            else if (val == 3)
            {
                fixed_charges = 380;
                amount = units * 12.53;
                surcharge = units * 3.61;
            }
            else if (val == 4)
            {
                fixed_charges = 360;
                amount = units * 12.13;
                surcharge = units * 3.61;
            }
            else
            {
                cout<<"Invalid input";
            }
        }
        else if(choice == 2)
        {
            cout<<"Please Select your category: \nFor 5-500 kW(at 400 V) press 1.\nFor all loads upto 5000KW(at 11,33KV) press 2.\nFor all loads upto 5000kW(at 66,132kV) press 3. \nFor all loads at 220KV & above press 4.";
            cin>>val;
            cout<<"Enter the units consumed during peak hours: ";
            cin>>units1;
            cout<<"Enter the units consumed during off-peak hours: ";
            cin>>units2;
            if (val == 1)
            {
                amount = (units1*18) + (units2 -12.08);
                surcharge = units2 *0.21;
                fixed_charges = 400;
            }
            else if (val == 2)
            {
                amount = (units1* 17.83) + (units2* 11.58);
                surcharge = (units1*0.17) + (units2 * 0.62);
                fixed_charges = 380;
            }
            else if(val == 3)
            {
                amount = (units1*17.33) + (units2*11.33);
                surcharge = (units1* 0.67) + (units2* 0.77);
                fixed_charges = 360;
            }
            else if(val == 4)
            {
                amount = (units1* 16.83)+(units2 * 11.18);
                surcharge = (units1*1.17) + (units2 * 0.92);
                fixed_charges = 340;
            }
        }
        meter_rent = 15.0;
        tvl = 60;
        electricity_duty = 0.02*(amount + surcharge);
        GST_retailers = 0;
        GST = 0.17 * (amount+surcharge+ meter_rent + electricity_duty );
        GST2 = 0.015 * (amount+surcharge+ meter_rent + electricity_duty);
        total_amount = amount+surcharge+ meter_rent + electricity_duty + GST +GST2 +GST_retailers+tvl+ bank_charges ;
        cout<<"FIxed charges: "<<fixed_charges<<endl;
    cout<<"Variable charges: "<<amount<<endl;
    cout<<"Surcharge: "<<surcharge;
    cout<<"\nMeter Rent: "<<meter_rent;
    cout<<"\nElectricty Duty: "<<electricity_duty;
    cout<<"\nGeneral Sales Tax: "<<GST<<endl;
    cout<<"2% Further GST: "<<GST2;
    cout<<"\nGST on retailers: "<<GST_retailers;
    cout<<"\nTV license fees: "<<tvl;
    cout<<"\nBank charges: "<<bank_charges<<endl;
    cout<<"The total amount billed is: "<<total_amount<<"Rs";
    }

main()
{
    char type;
    cout<<"\t\tElectricty Bill Calculator Made By EE-030"<<endl;
    cout<<"Select you category: Press R for residential, C for commercial, and I for industrial: ";
    cin>>type;
    if (type == 'R')
    {
        residential();
    }
    if (type == 'C')
    {
        commercial();
    }
    if (type == 'I')
    {
        industrial();
    }

}
