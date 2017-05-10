1) Used this program to decyrpt message.

**
 * Created by edmac on 5/9/17.
 */
public class CeasarDecrypt {

    public static void main(String[] args){

        String message = "Vefwoluibahgvul Xbpggpmf Vehglwht - npaobi kva jvt / yksvdl7921";
        String dMessage = "";
        int key = 1;
        char ch;

        do {

            for(int i = 0; i < message.length(); i++){
                ch = message.charAt(i);

                if(ch >= 'a' && ch <= 'z'){
                    ch = (char)(ch - key);

                    if(ch < 'a'){
                        ch = (char)(ch + 'z' - 'a' + 1);
                    }
                    dMessage += ch;
                }else if(ch >= 'A' && ch <= 'Z'){
                    ch = (char)(ch - key);

                    if(ch < 'A'){
                        ch = (char)(ch + 'Z' - 'A' +1);
                    }
                    dMessage += ch;

                }else {
                    dMessage += ch;
                }
            }

            System.out.println("Decrypted Message = " + dMessage + "\n");
            dMessage = "";
            key++;

        }while(key < 27);
    }
}
