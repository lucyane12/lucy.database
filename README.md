# Example

```
    <script>
      const zeev = new XMLHttpRequest();
      const method = "GET";
      const url = "https://lucyane12.github.io/lucy.database/parent.json";

      zeev.open(method,url,true);
      zeev.onreadystatechange = function(){
      if(this.readyState == 4 && this.status == 200){
        var data = JSON.parse(zeev.responseText);
        var y = Math.floor(Math.random()*data.length);
        var res = data[y].img;
        var web = `<img src="${res}" width="500px">`;
        document.getElementById("result").innerHTML = web;
      }
      };
      zeev.send();
    </script>
    
    <div id="result"></div>
```
### Note 
* This database does not support the use of  ``` forEach ```  !!!
