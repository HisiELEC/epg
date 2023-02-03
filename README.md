# EPG

  Repositório que contém os arquivos de mapeamento e canais das fontes EPG usadas pelo LibreELEC!
  
   
  Nele, temos arquivos .map que segue o formato abaixo:
  
    channel_id=nome_do_canal,nome_do_canal_2=numero_do_canal[opcional]
    
  Por exemplo, suponha que queremos mapear o canal <b>Telefe</b> e o <b>Telefe HD</b>.<br>
  Basta dar uma olhada no channels.xml da fonte EPG utilizada (pode ser que não tenha o canal) e pegar o channel id ou epg_id do canal. <br>
 ```xml
 <?xml version="1.0" encoding="UTF-8"?>
<tv>
 <channel id="100066">
  <display-name>Telefe</display-name>
 </channel>
 <channel id="100563">
  <display-name>TV China</display-name>
 </channel>
 ```
 
 Como podemos ver acima, o epg_id do canal é <b>100066</b>, agora criamos uma linha no arquivo .map com o id e os nomes dos canais:<br>
   ```map
   100066=Telefe,Telefe HD
   ```
