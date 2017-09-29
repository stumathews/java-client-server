import java.net.*;
import java.io.InputStream;
import java.io.OutputStream;
import java.io.BufferedWriter;
import java.io.PrintWriter;
public class JavaClient
{
    public static final int SERVER_PORT = 8080;
    public static final String SERVER_ADDRESS = "127.0.0.1";

    public static void main(String[] args) throws java.net.UnknownHostException, java.io.IOException
    {
	Socket socket = new Socket( SERVER_ADDRESS, SERVER_PORT );
	//InputStream clientInputStream = socket.getInputStream();
	OutputStream clientOutputStream = socket.getOutputStream();
	PrintWriter printWriter = new PrintWriter(clientOutputStream);
	printWriter.print("My Name is");
	printWriter.print("Stuart");
	printWriter.close();
	clientOutputStream.close();
	
    }

}