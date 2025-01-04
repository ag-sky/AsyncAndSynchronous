# AsyncAndSynchronous

Synchrousnly Fetching data and run it on main thread ( very bad)

public void fetchData(){
try{
  Url url = new URL("xyz.com");
  HTTPUrlConnection connection = (HTTPUrlConnection) url.openConnection()
;
BufferReader reader = new BufferReader(new InputStreamReader(connection.getInputStream());
StringBuilder response = new StringBuilder();
Stirng line;
while((line = reader.readLine) != null){
response.apeend(line)
}
reader.close
  } catch (Exception e) {
        e.printStackTrace();
    }
}
}

Synchrousnly Fetching data and run it on background thread (good but block thread)

public void fetchData(){
    ExecuterService executer = Executers.newSingleThreadExecution;
    executer.execute( -> {
    URL url = new URL("https://jsonplaceholder.typicode.com/posts/1");
            HttpURLConnection connection = (HttpURLConnection) url.openConnection();
            connection.setRequestMethod("GET");

            // Blocks only the background thread
            BufferedReader reader = new BufferedReader(new InputStreamReader(connection.getInputStream()));
            StringBuilder response = new StringBuilder();
            String line;
            while ((line = reader.readLine()) != null) {
                response.append(line);
            }
            reader.close();
          // to main thread.
            Handler(Looper.getmainlooper.post()-> {
            updateUI;
    ) catch(e:Exception{
    {
}finally{
executer.shutdown();
}


# asynchrously calling api ( background + not blocking thread)

public void Async{

public static void AsyncApi(){
 val client = new OkHTTP();
 }


 public void fetchData(){
    Request request = new Request.Builder()
    .url("xyx.com")
    .build

    client.call(request).enqueue( new Callback() {


    override fun onFailure(Call call, Exception e) {
    
}
override fun onSuccess(Call call, response){
}
response = responsebody.sstring()

Handler(looper.getmainlooper().post()->{update ui)
}





 }
















 
