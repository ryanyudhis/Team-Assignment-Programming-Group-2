# Team-Assignment-Programming-Group-2-Task 1

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int jumlah_orang;
        String nama;
        double makanan1_harga = 9999.99,
                makanan2_harga = 12345.67,
                makanan3_harga = 21108.40,
                makanan4_harga = 13579.13,
                makanan5_harga = 98765.43;

        System.out.println("Selamat Datang Di Restoran BUNGAR");
        // =======================Add Jumlah====================== //
        System.out.print("Pesanan untuk berapa orang? : ");
        jumlah_orang = input.nextInt();

        // =======================Add nama pemesan====================== //
        System.out.print("Pesanan atas nama : ");
        nama = input.nextLine();
        input.nextLine();

        // =======================Daftar Menu====================== //
        System.out.println("\n Menu Special hari ini");
        System.out.println("=======================");
        System.out.println("    1. Nasi Goreng Spesial       @ Rp. " + makanan1_harga);
        System.out.println("    2. Ayam Bakar Spesial        @ Rp. " + makanan2_harga);
        System.out.println("    3. Steak Sirloin Spesial     @ Rp. " + makanan3_harga);
        System.out.println("    4. Kwetiaw Siram Spesial     @ Rp. " + makanan4_harga);
        System.out.println("    5. Kambing Guling Spesial    @ Rp. " + makanan5_harga);
        System.out.println();

        // =======================Add Pesanan====================== //
        System.out.println("Pesanan Anda [Batas Pesanan 0-10 PO]");
        System.out.print("Nasi Goreng Spesial    = ");
        int A = input.nextInt();
        System.out.print("Ayam Goreng Spesial    = ");
        int B = input.nextInt();
        System.out.print("Steak Sirlon Spesial   = ");
        int C = input.nextInt();
        System.out.print("Kwetiaw Siram Spesial  = ");
        int D = input.nextInt();
        System.out.print("Kambing Guling Spesial = ");
        int E = input.nextInt();
        System.out.println();

        // =======================Proses====================== //
        double Menu1 = (A * makanan1_harga);
        double Menu2 = (B * makanan2_harga);
        double Menu3 = (C * makanan3_harga);
        double Menu4 = (D * makanan4_harga);
        double Menu5 = (E * makanan5_harga);
        double Total = Menu1 + Menu2 + Menu3 + Menu4 + Menu5;
        double Diskon = Total * 10 / (float) 100;
        double Total_bayar = Total - Diskon;
        double Pembelian_perorang = Total_bayar / jumlah_orang;

        // =================Harga Pembelian dan Pehitungan================ //
        System.out.println("Selamat menikmati makanan anda...");
        System.out.println();
        System.out.println("Pembelian : ");
        System.out.printf("\n1. Nasi Goreng Spesial      %d Porsi * 9999,99     = Rp. " + Menu1, A);
        System.out.printf("\n2. Ayam Goreng Spesial      %d Porsi * 12345,67    = Rp. " + Menu2, B);
        System.out.printf("\n3. Steak Sirloin Spesial    %d Porsi * 21108,40    = Rp. " + Menu3, C);
        System.out.printf("\n4. Kwetiaw Siram Spesial    %d Porsi * 13579,13    = Rp. " + Menu4, D);
        System.out.printf("\n5. Kambing Guling Spesial   %d Porsi * 98765,43    = Rp. " + Menu5, E);
        System.out.println("\t+");
        System.out.println("=====================================================================");
        System.out.println("Total Pembelian                                   = Rp. " + Total);
        System.out.println("Disc.10 % <Masa Promosi>                          = Rp. " + Diskon + "\t-");
        System.out.println("=====================================================================");
        System.out.println("Total Pembelian setelah disc 10 %                 = Rp. " + Total_bayar + "\t-");
        System.out.println("Pembelian per orang <untuk 8 orang>               = Rp. " + Pembelian_perorang + "\t-");
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
