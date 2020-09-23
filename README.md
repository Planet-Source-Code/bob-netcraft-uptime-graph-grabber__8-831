<div align="center">

## NetCraft Uptime Graph Grabber


</div>

### Description

This code will go out to http://uptime.netcraft.com and grab the uptime graph (if there is one) for your site. Each time the graph on netcraft.com is updated, this code will update the graph that is being displayed on your local site.
 
### More Info
 
Make sure your site has a uptime graph at netcraft.com by going to http://uptime.netcraft.com and entering your sites URL into the text field and hitting "Examine".

Code isn't the quickest as there is alot of HTML it has to crop.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Bob](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/bob.md)
**Level**          |Intermediate
**User Rating**    |5.0 (25 globes from 5 users)
**Compatibility**  |PHP 4\.0
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__8-1.md)
**World**          |[PHP](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/php.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/bob-netcraft-uptime-graph-grabber__8-831/archive/master.zip)





### Source Code

```
<?php
// Enter the URL of your site below
$site = "http://www.pscode.com";
// Do not change anything below
$url = "http://uptime.netcraft.com/up/graph/?mode_u=on&mode_w=on&site=$site&submit=Examine";
$fp = show_source($url,"r");
if(ereg("/up/graphs/.*..png",$fp,$info)){
echo "<img src='http://uptime.netcraft.com$info[0]' alt='Uptime Graph'>";
} else {
echo "Your site doesn't have an uptime graph.";
}
?>
```

