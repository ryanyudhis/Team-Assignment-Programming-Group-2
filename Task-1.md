# Team-Assignment-Programming-Group-2-Task 1

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        int jumlahOrang;
        String nama;
        double makanan1Harga = 9999.99,
                makanan2Harga = 12345.67,
                makanan3Harga = 21108.40,
                makanan4Harga = 13579.13,
                makanan5Harga = 98765.43;

        System.out.println("Selamat Datang Di Restoran BUNGAR");
        // =======================Add Jumlah====================== //
        System.out.print("Pesanan untuk berapa orang? : ");
        jumlahOrang = input.nextInt();

        // =======================Add nama pemesan====================== //
        System.out.print("Pesanan atas nama : ");
        nama = input.nextLine();
        input.nextLine();

        // =======================Daftar Menu====================== //
        System.out.println("\n Menu Special hari ini");
        System.out.println("=======================");
        System.out.println("    1. Nasi Goreng Spesial       @ Rp. " + makanan1Harga);
        System.out.println("    2. Ayam Bakar Spesial        @ Rp. " + makanan2Harga);
        System.out.println("    3. Steak Sirloin Spesial     @ Rp. " + makanan3Harga);
        System.out.println("    4. Kwetiaw Siram Spesial     @ Rp. " + makanan4Harga);
        System.out.println("    5. Kambing Guling Spesial    @ Rp. " + makanan5Harga);
        System.out.println();

        // =======================Add Pesanan====================== //
        System.out.println("Pesanan Anda [Batas Pesanan 0-10 PO]");
        System.out.print("Nasi Goreng Spesial    = ");
        int nasiGoreng = input.nextInt();
        System.out.print("Ayam Goreng Spesial    = ");
        int ayamGoreng = input.nextInt();
        System.out.print("Steak Sirlon Spesial   = ");
        int steakSirloin = input.nextInt();
        System.out.print("Kwetiaw Siram Spesial  = ");
        int kwetiawSiram = input.nextInt();
        System.out.print("Kambing Guling Spesial = ");
        int kambingGuling = input.nextInt();
        System.out.println();

        // =======================Proses====================== //
        double menu1 = (nasiGoreng * makanan1Harga);
        double menu2 = (ayamGoreng * makanan2Harga);
        double menu3 = (steakSirloin * makanan3Harga);
        double menu4 = (kwetiawSiram * makanan4Harga);
        double menu5 = (kambingGuling * makanan5Harga);
        double total = menu1 + menu2 + menu3 + menu4 + menu5;
        double discount = total * 10 / (float) 100;
        double totalBayar = total - discount;
        double pembelianPerorang = totalBayar / jumlahOrang;

        // =================Harga Pembelian dan Pehitungan================ //
        System.out.println("Selamat menikmati makanan anda...");
        System.out.println();
        System.out.println("Pembelian : ");
        System.out.printf("\n1. Nasi Goreng Spesial      " + nasiGoreng + " Porsi * 9999,99     = Rp. " + String.format("%.2f", menu1));
        System.out.printf("\n2. Ayam Goreng Spesial      " + ayamGoreng + " Porsi * 12345,67    = Rp. " + String.format("%.2f", menu2));
        System.out.printf("\n3. Steak Sirloin Spesial    " + steakSirloin + " Porsi * 21108,40    = Rp. " + String.format("%.2f", menu3));
        System.out.printf("\n4. Kwetiaw Siram Spesial    " + kwetiawSiram + " Porsi * 13579,13    = Rp. " + String.format("%.2f", menu4));
        System.out.printf("\n5. Kambing Guling Spesial   " + kambingGuling + " Porsi * 98765,43    = Rp. " + String.format("%.2f", menu5));
        System.out.println("\t+");
        System.out.println("=====================================================================");
        System.out.println("Total Pembelian                                   = Rp. " + String.format("%.2f", total));
        System.out.println("Disc 10 % <Masa Promosi>                          = Rp. " + String.format("%.2f", discount) + "\t-");
        System.out.println("=====================================================================");
        System.out.println("Total Pembelian setelah disc 10 %                 = Rp. " + String.format("%.2f", totalBayar));
        System.out.println("Pembelian per orang <untuk 8 orang>               = Rp. " + String.format("%.2f", pembelianPerorang));
        System.out.println("                   Terima kasih atas kunjungan anda. . .");
        System.out.println("                     ...tekan Enter untuk keluar...");
        try {
            System.in.read();
        } catch (Exception e) {
            System.exit(0);
        }
        System.exit(0);
        return;
    }
}
