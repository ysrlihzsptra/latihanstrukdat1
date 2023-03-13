import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<konsumsi> listkonsumsi = new ArrayList<>();
        konsumsi<makanan,minuman> breakfast = new konsumsi<>();
        konsumsi<makanan,minuman>lunch = new konsumsi<>();

        makanan roti = new makanan();
        roti.setNamahidangan("roti tawar");
        minuman susu = new minuman();
        susu.setNamahidangan("susu sapi");
        breakfast.setkonsumsi(roti,susu);
        listkonsumsi.add(breakfast);

        makanan nasi = new makanan();
        nasi.setNamahidangan("Nasi putih");
        minuman air = new minuman();
        air.setNamahidangan("air putih");
        lunch.setkonsumsi(nasi,air);
        listkonsumsi.add(lunch);

        System.out.println(("menu konsumsi");
        for (konsumsi<makanan,minuman>konsumsi : listkonsumsi){
            makanan makanan = konsumsi.getM();
            minuman minuman = konsumsi.getI();

            System.out.println(makanan.disantap());
            System.out.println(minuman.disantap());
        }

    }
}
