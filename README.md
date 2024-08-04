# PRODIGY_SD_01
First Task of Prodigy internship


import java.util.Locale;
import java.util.Scanner;
public class TempretureConversionSystem {
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        System.out.println("Enter The Temperature");
        int temp=sc.nextInt();
        System.out.println("Enter unit Celsius,Fahrenheit or Kelvin");
        String unit=sc.next().toLowerCase();


        switch(unit){
            case "celsius":
                System.out.println("celsiusToFahrenheit: "+celsiusToFahrenheit(temp));
                System.out.println("celsiusToKelvin:  "+celsiusToKelvin(temp));
                break;
            case "fahrenheit":
                System.out.println("FahrenheitToCelsius: "+fahrenheitToCelsius(temp));
                System.out.println("FahrenheitToKelvin:  "+fahrenheitToKelvin(temp));
                break;
            case "kelvin" :
                System.out.println("KelvinToCelsius: "+kelvinToCelsius(temp));
                System.out.println("KelvinToFahrenheit:  "+kelvinToFahrenheit(temp));
                break;
            default:
                System.out.println("Invalid unit");

        }


}
      static double celsiusToFahrenheit(int n){
        return (9.0/5.0*n)+32;
      }
     static double celsiusToKelvin(int n){
        return n+273.15;
    }
    static double fahrenheitToCelsius(int n){
         return ((5.0/9.0)*(n-32));
    }
    static double fahrenheitToKelvin( int n){
        return (5.0/9.0*(n-32))+273.15;
    }
    static double kelvinToCelsius(int n){
        return n-273.15;
    }

    static double kelvinToFahrenheit(int n){
        return (9.0/5.0*(n-273.15))+32;
    }


}
