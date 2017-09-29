import java.net.*;
import java.io.InputStream;
import java.io.OutputStream;
import java.io.BufferedReader;
import java.io.InputStreamReader;
public class JavaServer 
{
    public static final String SERVER_LOCATION = "http://localhost";
    public static final int SERVER_PORT = 8080;

    private static InputStream serverInputStream;
    private static OutputStream serverOutputStream;

    public static void main(String[] args) throws java.io.IOException
    {
	ServerSocket serverSocket = new ServerSocket(SERVER_PORT);
	System.out.println("Waiting for client connection on server port "+SERVER_PORT);
	Socket socket = serverSocket.accept();
	System.out.println("Recieved connection on server port "+ SERVER_PORT);
		serverInputStream = socket.getInputStream();
		InputStreamReader inputStreamReader = new InputStreamReader(serverInputStream);
		BufferedReader reader = new BufferedReader(inputStreamReader);
		
		String recivedData = reader.readLine();
		while( recivedData != null )
		{
		    System.out.println("Server recived this: "+ recivedData );
		    recivedData = reader.readLine();
		}
		
		reader.close();
		serverInputStream.close();
//	serverOutputStream = socket.getOutputStream();
	

    }
}