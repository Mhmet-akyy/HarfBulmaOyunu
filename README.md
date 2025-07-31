# HarfBulmaOyunu
import java.util.ArrayList;
import java.util.Scanner;

public class HarfBulmaOyunu {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // 1. Adım: 4 harften oluşan başlangıç listesi
        ArrayList<String> harfListesi = new ArrayList<>();
        harfListesi.add("a");
        harfListesi.add("b");
        harfListesi.add("c");
        harfListesi.add("d");

        // 2. Adım: Kullanıcıdan 4 defa harf al
        for (int i = 0; i < 4; i++) {
            System.out.print((i + 1) + ". harfi giriniz: ");
            String girilenHarf = scanner.nextLine().toLowerCase();

            // 3. Adım: Harf listede varsa "found" yap, yoksa ekle
            if (harfListesi.contains(girilenHarf)) {
                int index = harfListesi.indexOf(girilenHarf);
                harfListesi.set(index, "found");
                System.out.println("Harf bulundu, 'found' ile değiştirildi.");
            } else {
                harfListesi.add(girilenHarf);
                System.out.println("Harf listede yoktu, listeye eklendi.");
            }
        }

        // 4. Adım: Güncel listeyi yazdır
        System.out.println("\nGüncellenmiş Harf Listesi: " + harfListesi);
    }
}
