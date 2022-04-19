# sifre_olusturma
Java101_8 Hatalı girilen şifrenin sıfırlanması ve yeni şifrenin eski şifreyle aynılığının denetlenmesi

/*Ödev
Eğer şifre yanlış ise kullanıcıya şifresini sıfırlayıp sıfırlamayacağını sorun, eğer kullanıcı sıfırlamak isterse yeni girdiği şifrenin hatalı girdiği ve unuttuğu şifre ile aynı olmaması gerektiğini kontrol edip , şifreler aynı ise ekrana "Şifre oluşturulamadı, lütfen başka şifre giriniz." sorun yoksa "Şifre oluşturuldu" yazan programı yazınız. */

import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
	    
	    String username, password, bilgi, sifre;
	    int count;
	    Scanner input=new Scanner(System.in);
	    System.out.print("Kullanıcı adınızı giriniz : ");
	    username=input.nextLine();
	    System.out.print("şifrenizi giriniz : ");
	    password=input.nextLine();
	    
	    if(username.equals("java123") && password.equals("program123")) {
	        System.out.print("Giriş yaptınız! ");
	    }else{
	        System.out.println("username ya da password bilginiz hatalı ");
	        if(username!="java123"){
	        System.out.println("sıfırlamak ister misiniz ?");
	        Scanner inp=new Scanner(System.in);
	        System.out.print("şifrenizi sıfırlamak için 1'e basınız, ya da çıkış için herhangi bir tuşa basınız !");
	        bilgi=inp.nextLine();
	        if (bilgi.equals("1")) {
	            System.out.println("şifreniz sıfırlandı");
	            System.out.print("Lütfen yeni şifrenizi giriniz ");
	            Scanner in=new Scanner(System.in);
	            sifre=in.nextLine();
	            if((sifre.contains("program123"))) {
	                System.out.print("Yeni şifre eski ile aynı olamaz");
	                    }else
	                        System.out.print("şifre oluşturuldu");
	            
	        }else{
	            System.out.print("sonra tekrar deneyiniz");
	    }
	    }
	    }

	}
}
