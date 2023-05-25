# WCF-chat-and-Client-on-WPF-forms
Сетевой чат с сервисом WCF и клиенте на WPF формах
1.Запустить ChatHost.exe в каталоге \ChatHost\bin\Debug от админа.
2.Запустить несколько ChatClient клиентов в разных инстансах.

При размещении на реальных ПК установить в конфигах реальные адреса.
Также в проекте ChatClient в Reference обновить ссылки в зависимостях на проект ChatHost.
При добавлении \обновлении этой ссылки хост должен быть запущен.
Host:
App.config 
 <add baseAddress="http://localhost:8301" /> --адрес для автоматической подгрузки конфигурации mexBeh на клиенте
 <add baseAddress="net.tcp://localhost:8302" /> --адрес работы сервиса


Client:
App.config 
  <endpoint address="net.tcp://localhost:8302/" binding="netTcpBinding"
