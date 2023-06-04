# -.
在线提取旋风、雷霆、黑洞、蜜蜂等VPN软件的节点

一.进去黑洞、蜜蜂、旋风、雷霆等VPN软件的在线提取网址，全选复制密文到记事本（可通过多次刷新提取多个节点信息）
蜜蜂：https://www.09898434.xyz/api/evmess?
雷霆：https://www.lt71126.xyz:20000/api/evmess
旋风：https://www.xfjyqirx.xyz:20000/api/evmess
黑洞：https://www.hd327658.xyz:20000/api/evmess

二.
    1.打开Java在线网站，将下面文本复制进去
    
    
import java.security.MessageDigest;
import java.text.SimpleDateFormat;
import java.util.ArrayList;
import java.util.Calendar;
import java.util.Date;
import javax.crypto.Cipher;
import javax.crypto.spec.IvParameterSpec;
import javax.crypto.spec.SecretKeySpec;
import java.nio.charset.Charset;
import java.util.Base64;
public class HelloWorld {
    public static void main(String []args) throws Exception {
       
        String cipherText = "在此输入密文，多条用空格分割";
        
        String key = "ks9KUrbWJj46AftX"; //heidong\leiting\mifeng KEY
        //key = "awdtif20190619ti"; //xuanfen KEY
        
        String[] strArray=cipherText.split(" ");
        for (String text : strArray) {
          System.out.println(decrypt(text,key));
        }
    }
	public static String decrypt(String str, String str2) throws Exception {
		Cipher instance = Cipher.getInstance("AES/CBC/NoPadding");
		byte[] bytes = str2.getBytes(Charset.forName("UTF-8"));
		SecretKeySpec secretKeySpec = new SecretKeySpec(bytes, "AES");
		byte[] bytes2 = str2.getBytes(Charset.forName("UTF-8"));
		instance.init(2, secretKeySpec, new IvParameterSpec(bytes2));
		byte[] doFinal = instance.doFinal(Base64.getDecoder().decode(str));
		return new String(doFinal, Charset.forName("UTF-8"));
    }
}



Java在线网址：https://www.tutorialspoint.com/compile_java_online.php
   2.将复制的密文填入 String cipherText = "在此输入密文，多条用空格分割";
   3.点击左上角的Execute运行脚本，右侧会得到节点信息
   4.将复制的节点导入clash，v2rayN等软件
