# kdv
kdv oranı hesaplayan program
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        double tutar, kdvOran = 0.18, kdvTutar, kdvliTutar;

        Scanner input = new Scanner(System.in);
        System.out.print("ilk fiyatı giriniz : ");
        tutar = input.nextDouble();

        kdvTutar = tutar * kdvOran;
        kdvliTutar = tutar + kdvTutar;

        double kdvOrani = (tutar < 1000) ? 0.08 : 0.18;
        kdvTutar =tutar * kdvOrani;
        kdvliTutar=tutar + kdvTutar;

        System.out.println("Toplam fiyat: " + kdvliTutar);

        System.out.println("Kdv'siz Tutar :" + tutar);
        System.out.println("Kdv oranı :" + kdvOran);
        System.out.println("Kdv Tutarı :" + kdvTutar);
        System.out.println("Kdvli tutar :" + kdvliTutar);


    }
}
