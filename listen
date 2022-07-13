import java.io.BufferedReader;
import java.io.InputStream;
import java.io.InputStreamReader;
import java.net.Socket;

public class listen {
    public listen() {
    }
    public static void main(String[] args) throws Exception {
        BufferedReader in = new BufferedReader(new InputStreamReader(System.in));
        Socket sock = new Socket("INSERT VALID IP ADDRESS", 4000); //Initial Testing Was Done With My Private Wifi; I Removed This Address For Privacy Reasons
        InputStream inStream;
        try {
            inStream = sock.getInputStream();
        } catch (Throwable var8) {
            try {
                sock.close();
            } catch (Throwable var7) {
                var8.addSuppressed(var7);
            }
            throw var8;
        }
        sock.close();
        BufferedReader receive = new BufferedReader(new InputStreamReader(inStream));
        String receiveMessage;
        if ((receiveMessage = receive.readLine()) != null) System.out.println(receiveMessage);
        System.exit(0);
    }
}
