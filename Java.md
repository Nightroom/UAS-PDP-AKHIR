public class Manusia {
    String nama;
    int umur;
    char jeniskelamin;
    double tinggibadan;
    double beratbadan;
    String[] hobi;

    public Manusia(String nama, int umur, char jeniskelamin, double tinggibadan, double beratbadan, String[] hobi) {
        this.nama = nama;
        this.umur = umur;
        this.jeniskelamin = jeniskelamin;
        this.tinggibadan = tinggibadan;
        this.beratbadan = beratbadan;
        this.hobi = hobi;
    }

    public String getNama() {
        return nama;
    }

    public int getUmur() {
        return umur;
    }

    public char getJenisKelamin() {
        return jeniskelamin;
    }

    public double getTinggiBadan() {
        return tinggibadan;
    }

    public double getBeratBadan() {
        return beratbadan;
    }

    public String[] getHobi() {
        return hobi;
    }

    public void setNama(String nama) {
        this.nama = nama;
    }

    public void setUmur(int umur) {
        this.umur = umur;
    }

    public void setJenisKelamin(char jenisKelamin) {
        this.jeniskelamin = jenisKelamin;
    }

    public void setTinggiBadan(double tinggiBadan) {
        this.tinggibadan = tinggiBadan;
    }

    public void setBeratBadan(double beratBadan) {
        this.beratbadan = beratBadan;
    }

    public void setHobi(String[] hobi) {
        this.hobi = hobi;
    }

    public String getStatusBeratBadan() {
        double bmi = beratbadan / Math.pow(tinggibadan / 100, 2);

        if (bmi < 18.5) {
            return "Kekurangan berat badan";
        } else if (bmi >= 18.5 && bmi < 24.9) {
            return "Berat badan normal";
        } else if (bmi >= 25 && bmi < 29.9) {
            return "Kelebihan berat badan";
        } else {
            return "Obesitas";
        }
    }

    public static void main(String[] args) {
        Manusia[] manusiaArray = new Manusia[1];


        String[] hobiGanjar = {
            "Membaca",
            "Olahraga",
            "Menulis",
            "Memancing",
            "Menari",
            "Melawak"
        };
        manusiaArray[0] = new Manusia("Ganjar", 25, 'L', 170, 70, hobiGanjar);
        for (Manusia manusia : manusiaArray) {
            System.out.println("Nama: " + manusia.getNama());
            System.out.println("Umur: " + manusia.getUmur());
            System.out.println("Jenis Kelamin: " + manusia.getJenisKelamin());
            System.out.println("Tinggi Badan: " + manusia.getTinggiBadan());
            System.out.println("Berat Badan: " + manusia.getBeratBadan());
            System.out.println("Hobi: " + String.join(", ", manusia.getHobi()));
            System.out.println("Status Berat Badan: " + manusia.getStatusBeratBadan());
            System.out.println();
        }
    }
}
