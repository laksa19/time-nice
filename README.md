# time-nice
Reformat time status Mikrotik hotspot page status

```
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
</head>
<body>
<h3>1d30h54m21s</h3>
<h3 id="x">1d30h54m21s</h3>

<script>
$(document).ready(function(){
	$("#x").html();
    $.getJSON("https://mikhmon-api-mtn.sourceforge.io/?c="+$("#x").html()+"&json", function(result){
        $("#x").html(result["time_nice"]);
      });
    });
</script>
</body>
</html>

```
