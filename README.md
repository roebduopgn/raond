# raond
web3
import java.io.BufferedReader;
import java.io.InputStreamReader;

public class QuerySourceCode {
  public static void main(String[] args) {
    try {
      // 执行 javap 命令
      Process p = Runtime.getRuntime().exec("javap java.lang.String");
      
      // 读取命令的输出
      BufferedReader in = new BufferedReader(new InputStreamReader(p.getInputStream()));
      String line;
      while ((line = in.readLine()) != null) {
        System.out.println(line);
      }
    } catch (Exception e) {
      e.printStackTrace();
    }
  }
}
