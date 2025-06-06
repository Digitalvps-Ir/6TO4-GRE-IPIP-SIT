![R (2)](https://github.com/Azumi67/PrivateIP-Tunnel/assets/119934376/a064577c-9302-4f43-b3bf-3d4f84245a6f)
نام پروژه :  Geneve | anycast | 6TO4 | GRE | GRE6 | IP6IP6 | SIT | Erspan + IPsec- چندین سرور ایران و خارج
---------------------------------------------------------------
----------------------------------

**روش لوکال l2tp اضافه شد**(به قسمت مولتی روش l2tp مراجعه کنید)

**این پروژه صرفا برای آموزش و بالا بردن دانش بوده است و هدف دیگری در ان نمیباشد**

**برای ویرایش private ip از قسمت edit local مراجعه کنید**

**روش EOIP به همراه آموزش اضافه شد(روش های ترکیبی با EOIP شاید بعدا اضافه شود)**(پرایوت ایپی مربوطه را در فایروال باز کنید)

**ربات ریکانفیگ برای تک و مولتی سرور ها اضافه شد(ربات ریکانفیگ برای سرورهایی میباشد که مشکل قطعی لوکال در هر چند ساعت را دارند و تنها با reconfig مشکلشان حل میشود)**

**وایرگارد و چند روش ترکیبی داخل گزینه 4 اضافه شد (همراه با آموزش)**

**روش ISATAP به همراه آموزش اضافه شد***


![check](https://github.com/Azumi67/PrivateIP-Tunnel/assets/119934376/13de8d36-dcfe-498b-9d99-440049c0cf14)
**امکانات و نکات**

- دارای گزینه Status و نوع تانل شما و تعداد سرور آنلاین در هر سرور و ایپی ریموت سرور شما را نشان میدهد.
- امکان تانل های متفاوت که شامل IP6IP6 | 6TO4 | GRE6 | Geneve | Erspan + IPsec و غیره میشود
- امکان تانل 6TO4 و ANYCAST و IP6IP6 و GRE6 بین چندین سرور خارج و ایران
- امکان تانل ها VXLAN و سایر روش های آن
- امکان تانل EOIP
- امکان تانل l2tp
- امکان تانل وایرگارد و چند روش ترکیبی آن
- امکان تانل ISATAP به صورت سرور و کلاینت
- امکان ویرایش لوکال ایپی و سایر موارد
- دارای ربات ریکانفیگ
- امکان پورت فوروارد و تانل اصلی پس از اجرای 6TO4 و سایر تانل ها
- امکان تانل بین 5 سرور ایران و ده سرور خارج
- امکان تانل vxlan به صورت تک سرور به صورت three methods
- امکان تانل Geneve با چندین روش متفاوت (مولتی سرور و به صورت تکی)
- امکان تانل Geneve با IPsec ( مولتی و تکی)
- امکان تانل erspan همراه با ipsec ( مدل ساده آن بر بستر ایپی ورژن ۴ بر روی بعضی سرور های ایران کار نمیکند)
- امکان تانل gre6tap به صورت تکی و مولتی همراه با ipsec
- تانل Geneve +  Gre6 با دو روش NATIVE یا IPV4
- امکان حذف جداگانه
- دارای ریست تایمر برای چندین لوکال تانل و ریست تایم اجباری بر اساس پینگ
- امکان تانل بدون داشتن Native IPV6
- امکان تغییر دیفالت روت هم اضافه شد برای کسانی که مشکل نوسان دارند.
- حتما پرایوت ایپی ها را در پنل باز کنید تا کانفیگ های شما کار کند.
- اگر در فایروال خود پرایوت ایپی ها را بستید، ایپی مربوطه را در فایروال خود باز کنید (اگر نمیدانید چگونه ! در اینترنت سرچ بکنید)
- امکان ویرایش MTU به menu اضافه شد (کاهش packet loss)
---------------
- **حتما برای کانفیگ تانل های geneve، نخست فایروال ufw را خاموش کنید و پس از اتمام کانفیگ میتوانید روشن نمایید و حتما پس از روشن کردن آن، ufw reload هم بزنید اگر کار نکرد**
- **اگر فایروال روشن دارید و تانل gen کار نکرد، پس از هر بار ریبوت ممکن است نیاز باشد که یک بار بر روی هر دو سرور ufw reload بزنید وگرنه ممکن است تانل کار نکند.**
- **اگر یک روش کار نکرد روش های دیگر را امتحان کنید.**(اگر بعضی روش ها کار نکرد ، پس از uninstall، یک بار هم ریبوت نمایید)
- **در 6to4 روش anycast و بدون anycast احتمال از کار افتادن native میباشد و باید default route را فعال کنید**
-------

  <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/3cfd920d-30da-4085-8234-1eec16a67460" alt="Image"> آپدیت</strong></summary>
  
------------------------------------ 

- روش l2tp اضافه شد
- روش EOIP اضافه شد
- ربات ریکانفیگ اضافه شد
- اضافه شدن وایرگارد و چند روش آن
- اضافه شدن ویرایش لوکال ایپی و سایر موارد
- اضافه شدن ریست تایمر اجباری بر اساس پینگ و کاهش keepalive به پنج ثانیه
- گزینه ip forward برای ایپی 4 و 6 اضافه شد برای کسانی که مشکلات تانل داشتند
- گزینه ریست تایمر برای چندین لوکال تانل اضافه شد
- گزینه Status اضافه شد و نوع تانل شما و تعداد سرور آنلاین در هر سرور و ایپی ریموت سرور شما را نشان میدهد.(فیکس شد)
- آموزش Vxlan برای تک سرور قرار داده شد.
- تغییراتی در روت gre6, gre6tap و تمام Ipsec ها و تک سرور ها و پنج سرور ایران و 10 خارج انجام شد.
- ایپی اضافه برای Ipsec حذف شد از انجا که در داخل ecryption loop نبود.
- راهنمای نام اینترفیس و تانل به منوهای مربوطه اضافه شد Tunnel names guide
- ویرایش سرور اضافه شد
- 5 سرور ایران و 10 سرور خارج ( روش sit) اضافه شد
- ده سرور خارج اضافه شد
- محاسبه اتومات MTU به دلیل فاکتورهای زیاد و سرور های متنوع، حذف شد
- اضافه شدن ipsec به همه تانل ها
- اضافه شدن Geneve به همراه IPsec ( مولتی و تک سرور)
- اضافه شدن Gre6tap به همراه IPsec (روش های مختلف)
- اضافه شدن پنج سرور به IP6IP6 و Gre6
- تانل erspan همراه با ipsec اضافه شد
- مشکلات کار نکردن تانل ip6tnl بعد از ریبوت، برطرف شد
- مشکلات mtu در private ip چندین سرور برطرف شد
- مشکلات تنظیم دیفالت روت و MTU برطرف شد
- اضافه کردن گزینه روت برای gre6 + native gen
- تانل geneve با چندین روش متفاوت اضافه شد
- امکان تانل بین چندین سرور اضافه شد.
- چندین دستور ip اضافه شد
- امکان replace route اضافه شد
- ویرایش mtu به منو اضافه شد
- از این به بعد میتوانید MTU را خودتان تنظیم کنید یا به صورت اتوماتیک مانند قدیم انتخاب شود.
- گرینه yes برای ست کردن Mtu به صورت دستی و گزینه no برای ست کردن اتوماتیک میباشد.
- مشکل ذخیره نکردن ایپی های جدید Native IPV6 حل شد

  </details>
</div>

--------------------------------

 <div align="right">
  <details> 
    <summary><strong><img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/aa529e70-6eec-46bd-bec0-50fb1d9a4aa5" alt="Image"> نکات و خطا ها (مهم)</strong></summary>

- اگر خطای buffer size گرفتید، اطمینان پیدا کنید که هر دو طرف سرور قبلا تانل 6to4 ای فعال ندارند.
- اگر مشکلی در پینگ گرفتن داشتید، اطمینان پیدا کنید که ایپی ها را به درستی وارد کردید
- لطفا دقت کنید در زمان حذف پرایوت ایپی به اشتباه گزینه اشتباه را انتخاب نکنید. این اسکریپت بارها تست شده است و به درستی باید کار کند.
- اگر پرایوت ایپی به درستی حذف نشود، تانل انجام نمیشود
- اگر در فایروال خود پرایوت ایپی ها را بستید، ایپی مربوطه را در فایروال خود باز کنید (اگر نمیدانید چگونه ! در اینترنت سرچ بکنید)
- اطمینان پیدا کنید که پرایوت ایپی ها را در پنل هم بلاک نکرده اید که تانل کار نخواهد کرد.
- از edit mtu برای کاهش پکت لاس خود استفاده کنید. در هر دیتاسنتر میتواند متفاوت باشد.
- گزینه y به معنی تنظیم دستی mtu و گزینه n به معنی تنظیم اتوماتیک میباشد.
- مطمئن شوید که اسکریپت های دیگر، دستورات کرون من را پاک نمیکند وکرنه تانل از کار میوفتد.
  </details>
</div>

------------------------
<div align="right">
  <details>
    <summary><strong>توضیحات</strong></summary>
  
------------------------------------ 
- 6TO4: encapsulates IPv6 packets within IPv4 packets for communication across IPv4 networks.

- GRE: (Generic Routing Encapsulation): Versatile tunneling protocol for encapsulating various network layer protocols, including IPv6, within IPv4 packets.

- GRE6: Variant of GRE specifically designed for tunneling IPv6 packets, simplifying their encapsulation within IPv4 packets.

- IP6IP6 (IPv6 over IPv6): Allows direct tunneling of IPv6 packets over an existing IPv6 infrastructure.

- SIT (Simple Internet Transition): Lightweight encapsulation method for tunneling IPv6 packets over an IPv4 infrastructure, requiring minimal configuration.

- Geneve : (Generic Network Virtualization Encapsulation) is a network tunneling protocol that provides a mechanism for encapsulating and decapsulating network packets for virtualized environments. It is designed to enable efficient network virtualization and overlay network solutions in cloud computing, data centers, and software-defined networking (SDN) environments.

Geneve is an extension of the original Virtual Extensible LAN (VXLAN) protocol and addresses certain limitations of VXLAN. It provides enhanced scalability, extensibility, and flexibility for network virtualization. Geneve encapsulates the original network packets inside a new tunneling header, allowing these packets to traverse an underlay network while being associated with specific virtual networks or tenants.

  </details>
</div>

-----------------------

![6348248](https://github.com/Azumi67/PrivateIP-Tunnel/assets/119934376/398f8b07-65be-472e-9821-631f7b70f783)
**آموزش ویرایش لوکال ایپی و سایر موارد**
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>نمونه برای مثال </summary>
    
  
------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج و ایران** 

 <p align="right">
  <img src="https://github.com/user-attachments/assets/b6f1430e-2b11-4586-9392-f8db9f542680" alt="Image" />
</p>


**ممکن است اشتباهات جزیی در این اپدیت باشد.میتوانید در قسمت Issues به بنده اطلاع دهید. روش های دیگر هم شاید اضافه کنم**

- در این اپدیت میتوانید secret key، ایپی 4 ایران یا خارج و یا ایپی های پرایوت را تغییر دهید.
- وقتی ایپی پرایوتی عوض میشود تمام ایپی های پینگ سرویس و ipsec و دستورات ufw هم اپدیت و عوض میشود
- پس از انجام تغییرات گزینه save stuff را بزنید تا تغییرات اعمال شود
- ممکن است گاهی خطاهایی ببینید که کنارش don't mind this error باشد. از این خطاها گذرکنید
- بعدا خودم تست بیشتری انجام میدم چون تست تمام روش ها خیلی وقت گیر است و از توان من خارج است.

------------------

  </details>
</div>  

-----------------------
![6348248](https://github.com/Azumi67/PrivateIP-Tunnel/assets/119934376/398f8b07-65be-472e-9821-631f7b70f783)
**آموزش ریست تایمر**
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>نمونه برای مثال </summary>
    
  
------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج و ایران** 

 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/0d72d9ff-054a-4379-b09a-543a6420d782" alt="Image" />
</p>


**ریست تایمر گزینه 7 به صورت تست اضافه شد. این مورد برای کسانی میباشد که باز هم قطعی دارند . لطفا قبل از ان ریست تایمر ها را پاک کنید و لوکال خود را reconfig کنید ( اگر این مورد توانست مشکل را حل کند، در اپدیت بعدی از شما سوال میشود تا خودتان local downtime را مشخص کنید.میتوانید نخست خازج را کانفیگ کنید و سپس سرور ایران یا شاید هم زمان)**

- به دلیل تغیبر keepalive، همچنین میتوانید یک بار reconfig انجام دهید
- ریست لوکال باید جدا از کانفیگ لوکال تانل شما انجام شود
- سرویس ریست تایمر ipsec هم از کرون به سرویس تغییر یافت.
- ریست تایمر بیشتر برای کسانی هست که میخواهند در تایم خاصی، لوکال خود را ریست نمایند . به همه این روش ها ریست اجباری بر اساس نداشتن پینگ هم اضافه شده است
- به طور مثال اگر شما حتی زمان تایمر لوکال خود را 3 ساعت قرار داده باشید؛ اگر باز هم لوکال ها به هم پینگ نداشته باشند ، ریست اجباری انجام میشود و کاری به ریست تایمر 3 ساعت شما ندارد. پس نیازی نیست ریست تایمرلوکال بر حسب دقیقه بذارید چون به صورت پیش فرض ریست اجباری هم فعال میشود
- مورد دیگر این هست که از شما سوال میشود که ایا میخواهید هر 60 ثانیه بررسی شود که ipv4/6 فوروارد شما فعال است یا خیر و در صورت غیرفعال بودن آن برای شما فعال میکند. در صورت نیاز میتوانید این مورد را فعال نمایید.
- برای تک کانکشن و مولتی به منوی مربوطه خود وارد شوید و قبل از تغییر ریست تایمر؛ یک بار ریست تایمر برای لوکال مربوطه را پاک نمایید.
- سعی نمایید ریست تایمر برای سرور خارج و ایران هم زمان کانفیگ شود.

------------------

  </details>
</div>  

-----------------------
![6348248](https://github.com/Azumi67/PrivateIP-Tunnel/assets/119934376/398f8b07-65be-472e-9821-631f7b70f783)
**آموزش ربات ریکانفیگ**
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>نمونه برای مثال </summary>
    
  
------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج و ایران** 

 <p align="right">
  <img src="https://github.com/user-attachments/assets/98f87493-77a9-4ed6-ac05-7f9a6c55559c" alt="Image" />
</p>


- پس از کانفیگ سرور هایتان این گزینه را انتخاب نمایید و همان input ها را در اینجا بدهید . تعداد پینگ و زمان ping interval هم مشخص کنید
- تمام mtu و default route ها no انتخاب شده است
- سپس ریکانفیگ بدون دخالت شما انجام میشود. اول بین دو ایپی پرایوت به طور مثال به تعداد 5 پینگ میگیرد و اگر پاسخی دریافت نکند نخست کانفیگ را پاک و سپس ریکانفیگ میکند.
- برای مولتی مانند کانفیگ مولتی، داخل سرور مربوطه پس از این که کانفیگ انجام دادید.. Input های مربوطه را وارد کنید و مقدار Ping interval و تعداد پینگ را مشخص کنید.
- این ریکانفیگ از نسخه رم پایین تر استفاده خواهد کرد که مشکلی برای سرور شما در حین انجام آن به وجود نیاورد
- مولتی ها به ارامی اضافه میشوند چون زمان زیادی برای این کار نیاز است

------------------

  </details>
</div>  

------------------------

 ![6348248](https://github.com/Azumi67/PrivateIP-Tunnel/assets/119934376/398f8b07-65be-472e-9821-631f7b70f783)
**آموزش ویرایش سرور**
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش 6TO4  | ایپی پرایوت 6</summary>
    
  
------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج و ایران** 



- **من دو سرور خارج دارم و یک سرور ایران و میخوام یک سرور اضافه کنم**
- برای تمامی روش ها قابلیت ویرایش اضافه شده است و این آموزش، تنها دو بخش را توضیح میدهد.
- دقت کنید در اینجا سروری نیازی نیست که پاک شود. برای پاک کردن و اضافه کردن به قسمت بعدی مراجعه کنید که توضیح دادم.
- در سرور خارج، وارد گزینه edit servers میشوم و داخل گزینه  6to4 > 10 kharej 1 iran وارد میشوم. سپس گزینه خارج سوم را میزنم و سرور سوم خارج را اضافه میکنم.
- حالا اسکریپت را در سرور ایران اجرا میکنم و وارد گزینه edit servers میشوم و سپس وارد گزینه 6to4 < 10 kharej 1 iran میشوم
- گزینه 10 سرور خارج 1 سرور ایران را انتخاب میکنم و سپس گزینه 11 یعنی سرور ایران را انتخاب میکنم
- سرور سوم را انتخاب میکنم تا سرور سوم در ایران اضافه شود

------------------

  </details>
</div>  
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش 6TO4 IPSEC  | ایپی پرایوت 6</summary>
    
  
------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج و ایران** 



- **من سه سرور خارج دارم و یک سرور ایران و میخواهم سرور سوم را پاک کنم و دوباره اضافه کنم**
- وارد گزینه edit servers میشوم و گزینه Remove را انتخاب میکنم و داخل گزینه 6to4 IPsec وارد میشوم. سپس گزینه خارج سوم را میزنم و سرور سوم خارج را پاک میکنم.
- حالا اسکریپت را در سرور ایران اجرا میکنم و وارد گزینه edit servers میشوم و گزینه remove را انتخاب میکنم و سپس وارد گزینه 6to4 ipsec میشوم.
- گزینه 5 سرور خارج 1 سرور ایران را انتخاب میکنم و سپس گزینه 6 یعنی سرور ایران را انتخاب میکنم
- سرور سوم را انتخاب میکنم تا سرور سوم در ایران حذف شود.
- در اینجا از ما سوال میشود که سرور های ما هم اکنون چند تا است. چون یک سرور پاک کردیم پس 2 سرور خارج داریم.عدد 2 و secret key پیشین خود را وارد نمایید. اینکار برای reconfig ipsec میباشد
- حالا باید در سرور های خارج systemctl restart strong-azumi1 را وارد کنم.
- سپس هم در سرور خارج و هم در سرور ایران سرور سوم خارج را اضافه میکنم. بدین صورت میشود
- در سرور خارج، وارد گزینه edit servers > add > 6to4 ipsec > 5 kharej 1 iran میشوم. خارج سوم رو انتخاب میکنم
- حالا در سرور ایران، وارد گزینه edit servers > add > 6to4 ipsec > 5 kharej 1 iran میشوم . گزینه 6 یعنی سرور ایران را انتخاب میکنم و سرور سوم خارج را اضافه میکنم.

------------------

  </details>
</div>  

-------------------------------------

  ![6348248](https://github.com/Azumi67/PrivateIP-Tunnel/assets/119934376/398f8b07-65be-472e-9821-631f7b70f783)
**آموزش تک سرور**
<div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>مشاهده tunnel status </summary>
  
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **تک سرور** 

 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/0444ddb8-bcc2-48bb-82d9-3db4f6797cd9" alt="Image" />
</p>

- از این به بعد میتوانید secret key در صورت نصب ipsec هم مشاهده کنید و نام اینترفیس و نام تانل در اسکریپت که بتوانید به سادگی حذفش نمایید
- در این اسکرین من Private + IPsec را کانفیگ کردم و مشاهده میکنید که کاملا مشخص هست که کدام تانل کانفیگ شده است

------------------

  </details>
</div>

 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش Vxlan با IPsec به صورت P2P</summary>
  
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج** 

 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/c3402f06-c441-4b1e-b18b-0d60d73201d7" alt="Image" />
</p>

- **حتما برای کانفیگ تانل های Vxlan، نخست فایروال ufw را خاموش کنید و پس از اتمام کانفیگ میتوانید روشن نمایید**
- **حتما ufw reload را پس از اتمام کانفیگ در صورت داشتن فایروال، اجرا کنید**
- در این آموزش روش Vxlan P2P به همراه IPsec را به شما نشان میدهم.
- این تانل به صورت point to point میباشد و نیاز به وارد کردن ایپی سرور خارج و سرور ایران میباشد. این تانل میتواند هم با IPsec و هم بدون IPsec باشد
- سرور خارج را کانفیگ میکنیم. من ایپی لوکال آخر را میخواستم به صورت private ip 6 باشد. شما میتوانید گزینه private ipv4 را انتخاب کنید
- ایپی 4 ایران و خارج را وارد میکنم
- پورت مقصد را 5513 وارد میکنم. شما میتوانید هر پورتی بدهید.
- سکرت کی را ازومی وارد میکنم. شما میتوانید به صورت generate شده وارد نمایید( در هر دو طرف سرور باید یکسان باشد)
- پس از نصب ipsec از من سوال میشود که ایا میخواهید که خود اسکریپت، اینترفیس اصلی را پیدا کند ؟ من y را وارد کردم . شما میتوانید به صورت دستی وارد نمایید. به طور مثال ممکن است اینترفیس اصلی شما eth0 یا ens و یا سایر موارد باشد( این مورد گاهی اوقات به کار می آید و وجودش نیاز بوده است)
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- رول های فایروال به صورت خودکار اضافه میشود.


----------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**سرور ایران**

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/81758945-23a7-4e7a-b65d-d7e7120d36c9" alt="Image" />
</p>

- مانند کانفیگ سرور خارج پیش میروم.چون در سرور خارج، private ip به صورت ipv6 میباشد باید در این سرور هم به صورت private ipv6 باشد.
- سرور ایران را کانفیگ میکنیم.
- ایپی 4 ایران و خارج را وارد میکنم
- پورت را مانند سرور خارج عدد 5513 قرار میدهم
- سکرت کی را مانند سرور خارج، ازومی قرار میدهم.
- پس از نصب ipsec، از من سوال میشود که ایا میخواهم خود اسکریپت اینترفیس اصلی را پیدا کند یا به صورت manual وارد میکنم ؟ من y را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- رول های فایروال اضافه شد
- یادتان باشد که در صورت داشتن فایروال حتما ufw reload را بزنید که پینگ شما فعال شود( بهتر است کانفیگ را بدون فایروال انجام دهید و پس از روشن کنید)
------------------

  </details>
</div>
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش Vxlan بدون IPsec به صورت FDB</summary>
  
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج** 


 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/b5f2a189-aec7-4c57-bd5e-2248e7c5d81e" alt="Image" />
</p>

- **حتما برای کانفیگ تانل های Vxlan، نخست فایروال ufw را خاموش کنید و پس از اتمام کانفیگ میتوانید روشن نمایید**
- **حتما ufw reload را پس از اتمام کانفیگ در صورت داشتن فایروال، اجرا کنید**
- در این آموزش روش Vxlan FDB بدون IPsec را به شما نشان میدهم. با IPsec هم به همین صورت میباشد تنها با توجه به اینکه نیاز به وارد کردن secret key دارید.
- این تانل به صورت FDB و با Bridge میباشد و نیاز به وارد کردن ایپی سرور Remote میباشد. این تانل میتواند هم با IPsec و هم بدون IPsec باشد
- سرور خارج را کانفیگ میکنیم.من ایپی لوکال آخر را میخواستم به صورت private ip 6 باشد. شما میتوانید گزینه private ipv4 را انتخاب کنید
- ایپی 4 ایران را وارد میکنم
- پورت مقصد را 5513 وارد میکنم. شما میتوانید هر پورتی بدهید.
- پس از نصب bridge از من سوال میشود که ایا میخواهید که خود اسکریپت، اینترفیس اصلی را پیدا کند ؟ من y را وارد کردم . شما میتوانید به صورت دستی وارد نمایید. به طور مثال ممکن است اینترفیس اصلی شما eth0 یا ens و یا سایر موارد باشد( این مورد گاهی اوقات به کار می آید و وجودش نیاز بوده است)
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- رول های فایروال به صورت خودکار اضافه میشود.


----------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**سرور ایران**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/c6069b15-33bd-4653-8c36-b349c35c4d9b" alt="Image" />
</p>

- مانند کانفیگ سرور خارج پیش میروم.چون در سرور خارج، private ip به صورت ipv6 میباشد باید در این سرور هم به صورت private ipv6 باشد.
- سرور ایران را کانفیگ میکنیم.
- ایپی 4 خارج را وارد میکنم (سرور remote)
- پورت را مانند سرور خارج عدد 5513 قرار میدهم
- پس از نصب bridge، از من سوال میشود که ایا میخواهم خود اسکریپت اینترفیس اصلی را پیدا کند یا به صورت manual وارد میکنم ؟ من y را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- رول های فایروال اضافه شد
- یادتان باشد که در صورت داشتن فایروال حتما ufw reload را بزنید که پینگ شما فعال شود( بهتر است کانفیگ را بدون فایروال انجام دهید و پس از روشن کنید)
------------------

  </details>
</div>
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش Vxlan با Bridge & IP بدون IPsec</summary>
  
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج** 

 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/ddd7c796-dabd-43ae-9bbf-dc2ea9c61915" alt="Image" />
</p>

- **حتما برای کانفیگ تانل های Vxlan، نخست فایروال ufw را خاموش کنید و پس از اتمام کانفیگ میتوانید روشن نمایید**
- **حتما ufw reload را پس از اتمام کانفیگ در صورت داشتن فایروال، اجرا کنید**
- در این آموزش روش Vxlan With Bridge & IP بدون IPsec را به شما نشان میدهم. با IPsec هم به همین صورت میباشد تنها با توجه به اینکه نیاز به وارد کردن secret key دارید.
- این تانل به صورت دادن Remote IP input و با Bridge میباشد و نیاز به وارد کردن ایپی سرور Remote میباشد. این تانل میتواند هم با IPsec و هم بدون IPsec باشد
- سرور خارج را کانفیگ میکنیم.من ایپی لوکال آخر را میخواستم به صورت private ip 4 باشد. شما میتوانید گزینه private ipv6 را انتخاب کنید
- ایپی 4 ایران را وارد میکنم یا همون سرور remote را وارد میکنم
- پورت مقصد را 5513 وارد میکنم. شما میتوانید هر پورتی بدهید.
- پس از نصب bridge از من سوال میشود که ایا میخواهید که خود اسکریپت، اینترفیس اصلی را پیدا کند ؟ من y را وارد کردم . شما میتوانید به صورت دستی وارد نمایید. به طور مثال ممکن است اینترفیس اصلی شما eth0 یا ens و یا سایر موارد باشد( این مورد گاهی اوقات به کار می آید و وجودش نیاز بوده است)
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- برای mtu دو مورد برای کانفیگ خواهیم داشت. یک مورد برای vxlan device و یکی هم برای bridge. من به صورت manual هر دو mtu را وارد کردم. شما میتوانید به صورت خودکار انتخاب کنید.
- رول های فایروال به صورت خودکار اضافه میشود.


----------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**سرور ایران**

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/d0bff3b4-a5ed-4588-90af-e9b76c6bd4e9" alt="Image" />
</p>

- مانند کانفیگ سرور خارج پیش میروم
- سرور ایران را کانفیگ میکنیم.چون در سرور خارج، private ip به صورت ipv4 میباشد باید در این سرور هم به صورت private ipv4 باشد.
- ایپی 4 خارج را وارد میکنم (سرور remote)
- پورت را مانند سرور خارج عدد 5513 قرار میدهم
- پس از نصب bridge، از من سوال میشود که ایا میخواهم خود اسکریپت اینترفیس اصلی را پیدا کند یا به صورت manual وارد میکنم ؟ من y را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- برای mtu دو مورد برای کانفیگ خواهیم داشت. یک مورد برای vxlan device و یکی هم برای bridge. من به صورت manual هر دو mtu را وارد کردم. شما میتوانید به صورت خودکار انتخاب کنید.
- رول های فایروال اضافه شد
- یادتان باشد که در صورت داشتن فایروال حتما ufw reload را بزنید که پینگ شما فعال شود( بهتر است کانفیگ را بدون فایروال انجام دهید و پس از روشن کنید)
------------------

  </details>
</div>

 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش Geneve + GRE6 | ایپی پرایوت 4</summary>
  
  
------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج** 



 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/c9d176d3-56ca-42a4-88c4-729c98effd45" alt="Image" />
</p>

- **حتما برای کانفیگ تانل های geneve، نخست فایروال ufw را خاموش کنید و پس از اتمام کانفیگ میتوانید روشن نمایید**
- سرور خارج را کانفیگ میکنیم.
- ایپی 4 ایران و خارج را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- مسیر اصلی default route را تغییر میدهم. شما میتوانید اینکار را نکنید.
 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/00f6eb28-194c-4cd8-9cde-f55229f81749" alt="Image" />
</p>

- برای geneve تنظیم mtu رو به صورت اتوماتیک انتخاب میکنم. شما میتوانید گزینه yes را بزنید و به صورت دستی وارد نمایید.
- کانفیگ انجام شد و ایپی نهایی به شما نمایش داده میشود
- رول های فایروال اضافه شد تا ارتباط برقرار شود

----------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**سرور ایران**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/4c8edc1c-89ac-474c-9696-cf676e5df508" alt="Image" />
</p>

- سرور ایران را کانفیگ میکنیم.
- ایپی 4 ایران و خارج را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- مسیر اصلی default route را تغییر میدهم. شما میتوانید اینکار را نکنید.
 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/d56b7258-6249-4776-9cf5-06451e88e0fb" alt="Image" />
</p>

- برای geneve تنظیم mtu رو به صورت اتوماتیک انتخاب میکنم. شما میتوانید گزینه yes را بزنید و به صورت دستی وارد نمایید.
- کانفیگ انجام شد و ایپی نهایی به شما نمایش داده میشود
- رول های فایروال اضافه شد تا ارتباط برقرار شود

------------------

  </details>
</div>

 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش Geneve + IPSEC | ایپی پرایوت 6</summary>
  
  
------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج** 



 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/e6d39d8f-340c-4656-a3e7-14021bf491ff" alt="Image" />
</p>

- **حتما برای کانفیگ تانل های geneve، نخست فایروال ufw را خاموش کنید و پس از اتمام کانفیگ میتوانید روشن نمایید**
- سرور خارج را کانفیگ میکنیم.
- دقت نمایید برای IPSEC من از گزینه GENEVE ADDRESS استفاده میکنم
- ایپی 4 ایران را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- برای SECRET KEY میتوانید مانند من از AZUMI یا به صورت رندوم generate نمایید . باید در هر دو سرور مقدار یکسانی قرار بدید
- برای geneve تنظیم mtu رو به صورت اتوماتیک انتخاب میکنم. شما میتوانید گزینه yes را بزنید و به صورت دستی وارد نمایید.
- کانفیگ انجام شد و ایپی نهایی به شما نمایش داده میشود
- رول های فایروال اضافه شد تا ارتباط برقرار شود
- دقت نمایید این روش مانند سایرروش ها ممکن است در بعضی از دیتاسنتر ها بسته باشد و به منظور باگ برنامه و خرابی روش نیست.

----------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**سرور ایران**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/bb138b35-946f-41ef-a902-e0b907ebf5f1" alt="Image" />
</p>

- سرور ایران را کانفیگ میکنیم.
- دقت نمایید برای IPSEC من از گزینه GENEVE ADDRESS استفاده میکنم
- ایپی 4 ایران و خارج را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- برای SECRET KEY میتوانید مانند من از AZUMI یا به صورت رندوم generate نمایید . باید در هر دو سرور مقدار یکسانی قرار بدید
- برای geneve تنظیم mtu رو به صورت اتوماتیک انتخاب میکنم. شما میتوانید گزینه yes را بزنید و به صورت دستی وارد نمایید.
- کانفیگ انجام شد و ایپی نهایی به شما نمایش داده میشود
- رول های فایروال اضافه شد تا ارتباط برقرار شود

------------------

  </details>
</div>
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش Geneve + NATIVE + GRE6 | ایپی پرایوت 6</summary>
  
  
------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج** 


 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/8a1255fb-f5f7-49d9-9023-492beeb332f8" alt="Image" />
</p>

- **حتما برای کانفیگ تانل های geneve، نخست فایروال ufw را خاموش کنید و پس از اتمام کانفیگ میتوانید روشن نمایید**
- سرور خارج را کانفیگ میکنیم.
- چون میخواهم ایپی پرایوت من از نوع 6 باشد در قسمت GENEVE IP VERSION ، گزینه دوم ایپی 6 رو انتخاب میکنم تا ایپی پرایوت 6 به من بدهد
- ایپی 6 ایران و خارج را وارد میکنم. اگر سرور ایران شما، ایپی 6 ندارد... میتوانید از تانل بروکر هم استفاده نمایید.
- اگر ایپی 6 سرور خارج شما مناسب نبود میتوانید از EXTRA NATIVE IP، یک ایپی 6 دیگر برای سرور خارجتان بگیرید و از ان استفاده نمایید.
- اگرنمی دانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید


 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/b972a5c4-d2b7-4b98-af13-6190b9080f25" alt="Image" />
</p>

- برای geneve تنظیم mtu رو به صورت اتوماتیک انتخاب میکنم. شما میتوانید گزینه yes را بزنید و به صورت دستی وارد نمایید.
- کانفیگ انجام شد و ایپی نهایی به شما نمایش داده میشود
- برای پینگ سرویس، ایپی 4 سرور ایران را بدهید.
- رول های فایروال اضافه شد تا ارتباط برقرار شود

----------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**سرور ایران**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/29d78e09-9d7d-4b07-a2d3-ff4cc507f47a" alt="Image" />
</p>

- سرور ایران را کانفیگ میکنیم.
- در سرور خارج در قسمت GENEVE IP VERSION از ایپی 6 استفاده کردیم پس در سرور ایران هم از ایپی 6 استفاده میکنیم.
- ایپی 6 ایران و خارج را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/1f6f4810-05f2-44e2-9557-556d178c2ae5" alt="Image" />
</p>

- برای geneve تنظیم mtu رو به صورت اتوماتیک انتخاب میکنم. شما میتوانید گزینه yes را بزنید و به صورت دستی وارد نمایید.
- کانفیگ انجام شد و ایپی نهایی به شما نمایش داده میشود
- برای پینگ سرویس، ایپی 4 سرور ایران را بدهید.
- رول های فایروال اضافه شد تا ارتباط برقرار شود

------------------

  </details>
</div>
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش Geneve + NATIVE + IP6TNL + GRE6 | ایپی پرایوت 6</summary>
  
  
------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج** 


 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/8ff505d6-93e2-40fb-bf3d-b159eca45bf9" alt="Image" />
</p>

- **حتما برای کانفیگ تانل های geneve، نخست فایروال ufw را خاموش کنید و پس از اتمام کانفیگ میتوانید روشن نمایید**
- سرور خارج را کانفیگ میکنیم.
- چون میخواهم ایپی پرایوت من از نوع 6 باشد در قسمت GENEVE IP VERSION ، گزینه دوم ایپی 6 رو انتخاب میکنم تا ایپی پرایوت 6 به من بدهد
- ایپی 6 ایران و خارج را وارد میکنم. اگر سرور ایران شما، ایپی 6 ندارد... میتوانید از تانل بروکر هم استفاده نمایید.
- اگر ایپی 6 سرور خارج شما مناسب نبود میتوانید از EXTRA NATIVE IP، یک ایپی 6 دیگر برای سرور خارجتان بگیرید و از ان استفاده نمایید.
- اگرنمی دانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید


 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/4259352e-9a5a-425e-b41f-067543e90d7c" alt="Image" />
</p>

- برای geneve تنظیم mtu رو به صورت اتوماتیک انتخاب میکنم. شما میتوانید گزینه yes را بزنید و به صورت دستی وارد نمایید.
- کانفیگ انجام شد و ایپی نهایی به شما نمایش داده میشود
- برای پینگ سرویس، ایپی 4 سرور ایران را بدهید.
- رول های فایروال اضافه شد تا ارتباط برقرار شود

----------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**سرور ایران**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/a3c23960-8f23-436f-ba16-001d98fc58cb" alt="Image" />
</p>

- سرور ایران را کانفیگ میکنیم.
- در سرور خارج در قسمت GENEVE IP VERSION از ایپی 6 استفاده کردیم پس در سرور ایران هم از ایپی 6 استفاده میکنیم.
- ایپی 6 ایران و خارج را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/99170117-c5b9-4a22-9cbf-eca477fb6812" alt="Image" />
</p>

- برای geneve تنظیم mtu رو به صورت اتوماتیک انتخاب میکنم. شما میتوانید گزینه yes را بزنید و به صورت دستی وارد نمایید.
- کانفیگ انجام شد و ایپی نهایی به شما نمایش داده میشود
- برای پینگ سرویس، ایپی 4 سرور ایران را بدهید.
- رول های فایروال اضافه شد تا ارتباط برقرار شود

------------------

  </details>
</div>
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش Geneve Method 2 | پرایوت ایپی 4</summary>
  
  
------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج** 



 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/a07b5e50-73d5-444e-af0d-56038a39b101" alt="Image" />
</p>

- **حتما برای کانفیگ تانل های geneve، نخست فایروال ufw را خاموش کنید و پس از اتمام کانفیگ میتوانید روشن نمایید**
- سرور خارج را کانفیگ میکنیم.
- در قسمت GENEVE IP VERSION ، پرایوت ایپی 4 را انتخاب میکنم
- ایپی 4 ایران را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- ایپی ساخته شده شما در آخر به شما نمایش داده میشود

----------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**سرور ایران**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/ee26ca1e-faf9-4b27-a00a-f42c09c2958d" alt="Image" />
</p>


- سرور ایران را کانفیگ میکنیم.
- در سرور خارج و در قسمت GENEVE IP VERSION ، پرایوت ایپی 4 را انتخاب کردیم
- ایپی 4  ایران را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- ایپی ساخته شده در اخر به شما نمایش داده میشود.
------------------

  </details>
</div>
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش Geneve Method 2 | پرایوت ایپی 6</summary>
  
  
------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج** 


 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/b67cee71-ad77-4223-9f9f-086503ccb8b4" alt="Image" />
</p>

- **حتما برای کانفیگ تانل های geneve، نخست فایروال ufw را خاموش کنید و پس از اتمام کانفیگ میتوانید روشن نمایید**
- سرور خارج را کانفیگ میکنیم.
- در قسمت GENEVE IP VERSION ، پرایوت ایپی 6 را انتخاب میکنم
- ایپی 4 ایران را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- ایپی 4 سرور ایران را برای سرویس پینگ وارد میکنم.
- ایپی ساخته شده شما در آخر به شما نمایش داده میشود

----------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**سرور ایران**

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/57ded48c-3972-4f5b-b6e1-17b794197af2" alt="Image" />
</p>


- سرور ایران را کانفیگ میکنیم.
- در سرور خارج و در قسمت GENEVE IP VERSION ، پرایوت ایپی 6 را انتخاب کردیم
- ایپی 4 سرور خارج را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- ایپی 4 سرور خارج را برای سرویس پینگ وارد میکنم.
- ایپی ساخته شده در اخر به شما نمایش داده میشود.
------------------

  </details>
</div>
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش Geneve Method 1 | پرایوت ایپی 4</summary>
  
  
------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج** 


 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/30851e2f-4b26-4b90-97af-6a17eca1f8d0" alt="Image" />
</p>

- **حتما برای کانفیگ تانل های geneve، نخست فایروال ufw را خاموش کنید و پس از اتمام کانفیگ میتوانید روشن نمایید**
- سرور خارج را کانفیگ میکنیم.
- در قسمت GENEVE IP VERSION ، پرایوت ایپی 4 را انتخاب میکنم
- ایپی 4 ایران را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- ایپی ساخته شده شما در آخر به شما نمایش داده میشود

----------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**سرور ایران**

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/9a7de8d9-d362-420b-b475-c98261f1e0cf" alt="Image" />
</p>


- سرور ایران را کانفیگ میکنیم.
- در سرور خارج و در قسمت GENEVE IP VERSION ، پرایوت ایپی 4 را انتخاب کردیم
- ایپی 4 ایران را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- ایپی ساخته شده در اخر به شما نمایش داده میشود.
------------------

  </details>
</div>
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش Geneve Method 1 | پرایوت ایپی 6</summary>
  
  
------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج** 


 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/6c0d0159-4ee6-4959-86d7-51237256c632" alt="Image" />
</p>

- **حتما برای کانفیگ تانل های geneve، نخست فایروال ufw را خاموش کنید و پس از اتمام کانفیگ میتوانید روشن نمایید**
- سرور خارج را کانفیگ میکنیم.
- در قسمت GENEVE IP VERSION ، پرایوت ایپی 6 را انتخاب میکنم
- ایپی 4 ایران را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- ایپی 4 سرور ایران را برای سرویس پینگ وارد میکنم.
- ایپی ساخته شده شما در آخر به شما نمایش داده میشود

----------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**سرور ایران**

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/fe62d05f-2b5c-4d44-94f2-724530eea3df" alt="Image" />
</p>


- سرور ایران را کانفیگ میکنیم.
- در سرور خارج و در قسمت GENEVE IP VERSION ، پرایوت ایپی 6 را انتخاب کردیم
- ایپی 4 خارج را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- ایپی 4 سرور خارج را برای سرویس پینگ وارد میکنم.
- ایپی ساخته شده در اخر به شما نمایش داده میشود.
------------------

  </details>
</div>
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش Geneve + Native | پرایوت ایپی 4</summary>
  
  
------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج** 

 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/e5aabf75-d238-42f7-874e-461893c88746" alt="Image" />
</p>

- **حتما برای کانفیگ تانل های geneve، نخست فایروال ufw را خاموش کنید و پس از اتمام کانفیگ میتوانید روشن نمایید**
- سرور خارج را کانفیگ میکنیم.
- در قسمت GENEVE IP VERSION ، پرایوت ایپی 4 را انتخاب میکنم
- ایپی 6 ایران را وارد میکنم. میتوانید از طریق تانل بروکر، ایپی 6 بگیرید و ان را وارد کنید یا اگر سرور شما ایپی 6 دارد ، ان را وارد کنید. (اتصال شما به خوب بودن و نداشتن اختلال بر روی این ایپی 6، بستگی دارد)
- اگر ایپی 6 سرور خارج شما مناسب نبود میتوانید از EXTRA NATIVE IP، یک ایپی 6 دیگر برای سرور خارجتان بگیرید و از ان استفاده نمایید.
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- ایپی 4 سرور ایران را برای سرویس پینگ وارد میکنم.
- ایپی ساخته شده شما در آخر به شما نمایش داده میشود

----------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**سرور ایران**

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/735da7cf-3cdf-4e98-87f0-04796fa27fb3" alt="Image" />
</p>


- سرور ایران را کانفیگ میکنیم.
- در سرور خارج و در قسمت GENEVE IP VERSION ، پرایوت ایپی 4 را انتخاب کردیم
- ایپی 6 خارج را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- ایپی 4 سرور خارج را برای سرویس پینگ وارد میکنم.
- ایپی ساخته شده در اخر به شما نمایش داده میشود.
------------------

  </details>
</div>
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش Geneve + Native | پرایوت ایپی 6</summary>
  
  
------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج** 

 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/44496990-8b3f-44e2-9a41-61515b616bf4" alt="Image" />
</p>

- **حتما برای کانفیگ تانل های geneve، نخست فایروال ufw را خاموش کنید و پس از اتمام کانفیگ میتوانید روشن نمایید**
- سرور خارج را کانفیگ میکنیم.
- در قسمت GENEVE IP VERSION ، پرایوت ایپی 6 را انتخاب میکنم
- ایپی 6 ایران را وارد میکنم. میتوانید از طریق تانل بروکر، ایپی 6 بگیرید و ان را وارد کنید یا اگر سرور شما ایپی 6 دارد ، ان را وارد کنید. (اتصال شما به خوب بودن و نداشتن اختلال بر روی این ایپی 6، بستگی دارد)
- اگر ایپی 6 سرور خارج شما مناسب نبود میتوانید از EXTRA NATIVE IP، یک ایپی 6 دیگر برای سرور خارجتان بگیرید و از ان استفاده نمایید.
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- ایپی 4 سرور ایران را برای سرویس پینگ وارد میکنم.
- ایپی ساخته شده شما در آخر به شما نمایش داده میشود

----------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**سرور ایران**

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/8337f2ef-6dcc-4300-8be4-07aa0842d00f" alt="Image" />
</p>


- سرور ایران را کانفیگ میکنیم.
- در سرور خارج و در قسمت GENEVE IP VERSION ، پرایوت ایپی 6 را انتخاب کردیم
- ایپی 6 خارج را وارد میکنم
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- ایپی 4 سرور خارج را برای سرویس پینگ وارد میکنم.
- ایپی ساخته شده در اخر به شما نمایش داده میشود.
------------------

  </details>
</div>

 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش IP6IP6</summary>
  
  
------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج** 



 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/5bfbbea6-4543-48c1-a2f5-d6b617f7ebec" alt="Image" />
</p>

- سرور خارج را کانفیگ میکنیم.
- ایپی 4 خارج و ایران را میدهیم.
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- تعداد ایپی اضافه هم یک عدد وارد میکنم
- اگر نوسانی ندارید میتوانید مسیر روت را تغییر ندهید. برای این آموزش من مسیر روت را تغییر دادم.
- اگر مسیر روت را تغییر داد و میخواهید این تانل را پاک کنید ، سرور هایتان را پس از پاک کردن ، یک بار ریبوت هم بکنید.
- و هم چنین دوباره گزینه No را برای ست کردن mtu، انتخاب میکنم. اگر آگاهی کافی دارید، mtu مناسب خود را بیابید.


----------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**سرور ایران**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/ddf0ccf1-aa3d-45ec-ab8d-5a722cebc100" alt="Image" />
</p>


- سرور ایران را کانفیگ میکنیم.
- ایپی 4 خارج و ایران را میدهیم.
- اگرنمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- تعداد ایپی اضافه هم یک عدد وارد میکنم
- اگر نوسانی ندارید میتوانید مسیر روت را تغییر ندهید. برای این آموزش من مسیر روت را تغییر دادم.
- اگر مسیر روت را تغییر داد و میخواهید این تانل را پاک کنید ، سرور هایتان را پس از پاک کردن ، یک بار ریبوت هم بکنید.
- و هم چنین دوباره گزینه No را برای ست کردن mtu، انتخاب میکنم. اگر آگاهی کافی دارید، mtu مناسب خود را بیابید.
- اگر در ufw و یا هر فایروالی، ایپی پرایوت را بستید، این ایپی مورد نظر را در فایروال خود باز کنید.
- با دستور ip a میتوانید ایپی خود را مشاهده کنید.

------------------

  </details>
</div>


 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش GRE</summary>
  

------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج**


 <p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/d63c344a-05c6-4218-84c2-21b6e9ed9c5b" alt="Image" />
</p>

- کانفیگ را از سرور خارج شروع میکنیم
- ایپی 4 سرور ایران و خارج را وارد نمایید
- تعداد ایپی مورد نیاز خود را وارد نمایید. به طور مثال 2 تا
- از ایپی های generate شده برای تانل استفاده نمایید یا با دستور ip a، ایپی های ساخته شده را ببینید
- ایپی ادرس 4 سرور ایران را برای فعال کردن سرویس پینگ وارد نمایید
- در اینجا هم میتوانید مسیر روت را تغییر دهید و همچنین MTU را دستی ست نمایید

----------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**سرور ایران**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/d17bda7e-2d10-4de3-b76c-6af385492ddf" alt="Image" />
</p>

- ایپی 4 سرور ایران و خارج را وارد نمایید
- تعداد ایپی مورد نیاز خود را وارد نمایید. به طور مثال 2 تا
- از ایپی های generate شده برای تانل استفاده نمایید یا با دستور ip a، ایپی های ساخته شده را ببینید
- ایپی ادرس 4 سرور خارج را برای فعال کردن سرویس پینگ وارد نمایید
------------------
  </details>
</div>  
<div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش ISATAP یک سرور خارج و دو کلاینت ایران</summary>

---------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور خارج**



<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/d133cd7e-05c7-4fcd-98f2-9142738b0875" alt="Image" />
</p>

- تمام تلاشم را کرده ام که در این روش، شما نیاز نباشد که به صورت manual پرفیکس هایی که ایجاد میشود را در سرور اصلی وارد کنید چون نیاز بود که در هنگام کانفیگ بین سرور و کلاینت در گردش باشید. بنابراین در حال حاضر باید نخست سرور خارج را کانفیگ کرد و سپس کلاینت های ایران را کانفیگ کرد
- مورد دیگری که هست در اینجا من سرور را خارج در نظر میگیرم و کلاینت را ایران. میتوان سرور را ایران در نظر گرفت و کلاینت ها خارج باشد که در اموزش دیگری قرار خواهم داد
- هم چنین در این روش از ریست لوکال استفاده میکنم که به صورت تست میباشد و در صورت استفاده میتوانید کارایی این مورد را با من در میان بگذارید.
- اگر این روش کارکرد خوبی داشت، 5 سرور و 5 کلاینت هم اضافه میکنم
- خب من 1 سرور خارج و 2 کلاینت ایران دارم.
- نخست ایپی 4 سرور خارج را وارد میکنم
- از من پرسیده میشود که mtu را به صورت manual وارد میکنید یا خیر. من n را وارد میکنم
- ایپی پرایوت شما نمایش داده میشود و سپس از من سوال میشود که چه تعداد کلاینت ایران دارم. من دو عدد کلاینت ایران دارم پس عدد 2 را وارد میکنم.
- ایپی 4 کلاینت اول ایران و پورت مورد نظر را وارد میکنم ( برای هر کلاینت باید پورت متفاوتی بدهید و ufw این پورت را به فایروال اضافه میکند)
- ایپی 4 کلاینت دوم ایران و پورت مورد نظر را وارد میکنم
- اگر از ufw استفاده میکنید بهتر است قبل از انجام کانفیگ، آن را disable کنید و سپس enable کنید یا ufw reload
- نخست از من سوال میشود که چند سرور ایران دارم. من دو سرور ایران دارم پس عدد 2 را وارد میکنم.
- سپس از من سوال میشود که ایا IPSEC فعال شود که من y را وارد میکنم و سپس secret key را azumi وارد میکنم ( شما میتوانید پیچیده تر بذارید)

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/84c50c16-e0f7-4af3-9df2-f19937ed2bad" alt="Image" />
</p>

- سپس از من میپرسد که ریست تایمر IPSEC بر چه اساس و unit ای باشد. من دقیقه را وارد میکنم و عدد 2 را وارد میکنم. مقدار شما میتواند متفاوت باشد
- سپس از من سوال میشود که ایا میخواهم لوکال من بر اساس زمانی خاص ریست شود که برای تست من گزینه y را وارد میکنم و به طور مثال هر ساعت میخواهم که این ریست انجام شود
- دقت نمایید شما میتوانید گزینه n را وارد کنید و ریست تایمر لوکال را فعال نکنید.
- اگر خطای بافر سایز گرفتید لطفا اطمینان حاصل فرمایید که روش های قبلی که در تضاد است ، پاک کرده باشید.
- از طریق گزینه Status میتوانید از فعال بودن روش و ایپی های کلاینت و سایر موارد آگاه شوید.

---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **کلاینت ایران اول**

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/ae812ca8-95f2-4eb6-bb89-c24f96683738" alt="Image" />
</p>

- کلاینت ایران اول را کانفیگ میکنم.
- ایپی 4 کلاینت اول ایران را وارد میکنم
- سپس ایپی 4 سرور را وارد میکنم و به صورت اتومات prefix سرور خارج در کلاینت اضافه میشود.
- پورتی که برای کلاینت ایران اول را وارد کرده بودم را اینجا وارد میکنم که 5050 بود
- از من سوال میشود که mtu را manual وارد کنم که n را میزنم تا اتومات انتخاب شود.
- ایپی پرایوت این کلاینت نمایش داده میشود و سپس از من سوال میشود که آیا IPSEC فعال شود یا خیر که من y را وارد میکنم تا فعال شود
- سپس از من سوال میشود که ریست تایمر IPSEC چه باشد که من 2 دقیقه قرار میدهم. شما میتوانید مقدار دیگری قرار دهید

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/99125f0b-470f-4dad-b5e2-bf1bc5a03828" alt="Image" />
</p>

- سپس از من سوال میشود که ایا میخواهم لوکال تانل من بر اساس بازه زمانی خاصی، ریست شود که من y را وارد میکنم و مقدار یک ساعت را وارد میکنم. شما میتوانید n بزنید که غیرفعال شود یا مقدار دیگری برای زمان انتخاب نمایید.(این عدد ها قابل تغییر است و فقط برای نمونه استفاده شده است)

---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **کلاینت ایران دوم**

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/e872f99d-88a3-4304-8106-94e981291aa9" alt="Image" />
</p>

- کلاینت ایران دوم را کانفیگ میکنم.
- ایپی 4 کلاینت دوم ایران را وارد میکنم
- سپس ایپی 4 سرور را وارد میکنم و به صورت اتومات prefix سرور خارج در کلاینت دوم اضافه میشود.
- پورتی که برای کلاینت ایران دوم را وارد کرده بودم را اینجا وارد میکنم که 5051 بود
- از من سوال میشود که mtu را manual وارد کنم که n را میزنم تا اتومات انتخاب شود.
- ایپی پرایوت این کلاینت نمایش داده میشود و سپس از من سوال میشود که آیا IPSEC فعال شود یا خیر که من y را وارد میکنم تا فعال شود
- سپس از من سوال میشود که ریست تایمر IPSEC چه باشد که من 2 دقیقه قرار میدهم. شما میتوانید مقدار دیگری قرار دهید

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/d34e615d-3e68-48d6-b27c-910d985dd1dc" alt="Image" />
</p>

- سپس از من سوال میشود که ایا میخواهم لوکال تانل من بر اساس بازه زمانی خاصی، ریست شود که من y را وارد میکنم و مقدار یک ساعت را وارد میکنم. شما میتوانید n بزنید که غیرفعال شود یا مقدار دیگری برای زمان انتخاب نمایید.(این عدد ها قابل تغییر است و فقط برای نمونه استفاده شده است)

---------------
 </details>
</div>
  </details>
</div>

 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش 6TO4</summary>
  
  
------------------------------------ 

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور خارج**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/bbe3e8ba-9b2d-4dec-a8dd-dce7345accf2" alt="Image" />
</p>

- ایپی 4 سرور ایران و خارج را وارد نمایید
- تعداد ایپی مورد نیاز خود را وارد نمایید. به طور مثال 2 تا
- از ایپی های generate شده برای تانل استفاده نمایید یا با دستور ip a، ایپی های ساخته شده را ببینید
- ایپی ادرس 4 سرور ایران را برای فعال کردن سرویس پینگ وارد نمایید
- اگر نمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- تعداد ایپی اضافه هم یک عدد وارد میکنم
- اگر نوسانی ندارید میتوانید مسیر روت را تغییر ندهید. برای این آموزش من مسیر روت را تغییر دادم.
- اگر مسیر روت را تغییر داد و میخواهید این تانل را پاک کنید ، سرور هایتان را پس از پاک کردن ، یک بار ریبوت هم بکنید.


---------------------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور ایران**



<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/2a89cd90-af70-484c-b8fa-60bd3d08699e" alt="Image" />
</p>

- سرور ایران را کانفیگ میکنیم.
- ایپی 4 سرور ایران و خارج را وارد نمایید
- تعداد ایپی مورد نیاز خود را وارد نمایید. به طور مثال 2 تا
- از ایپی های generate شده برای تانل استفاده نمایید یا با دستور ip a، ایپی های ساخته شده را ببینید
- ایپی ادرس 4 سرور ایران را برای فعال کردن سرویس پینگ وارد نمایید
- اگر نمیدانید چه mtu مناسب شما هست گزینه No رو بزنید. بعدا میتوانید در منو آن را ویرایش کنید
- تعداد ایپی اضافه هم یک عدد وارد میکنم
- اگر نوسانی ندارید میتوانید مسیر روت را تغییر ندهید. برای این آموزش من مسیر روت را تغییر دادم.
- اگر مسیر روت را تغییر داد و میخواهید این تانل را پاک کنید ، سرور هایتان را پس از پاک کردن ، یک بار ریبوت هم بکنید.

------------------

  </details>
</div>

 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش 6TO4 روت anycast</summary>
  
  
------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور خارج**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/1c53419e-dcbe-43b5-aacf-570e0f2c37c6" alt="Image" />
</p>

- ایپی 4 سرور خارج را وارد نمایید
- تعداد ایپی مورد نیاز خود را وارد نمایید. به طور مثال 2 تا
- از ایپی های generate شده برای تانل استفاده نمایید یا با دستور ip a، ایپی های ساخته شده را ببینید
- ایپی ادرس 4 سرور ایران را برای فعال کردن سرویس پینگ وارد نمایید
- اگر در تنظیم MTU اطلاعاتی ندارید، گزینه no را بزنید که به صورت اتوماتیک ست شود
          
---------------------------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور ایران**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/5207faf2-3d0f-43dc-90a7-9ea14c536d40" alt="Image" />
</p>

- ایپی 4 سرور ایران را وارد نمایید
- تعداد ایپی مورد نیاز خود را وارد نمایید. به طور مثال 2 تا
- از ایپی های generate شده برای تانل استفاده نمایید یا با دستور ip a، ایپی های ساخته شده را ببینید
- ایپی ادرس 4 سرور خارج را برای فعال کردن سرویس پینگ وارد نمایید
- اگر در تنظیم MTU آطلاعاتی ندارید، گزینه no را بزنید.
-  در صورت نوسان، مسیر روت را مانند من تغییر دهید. گزینه YES تغییر میدهد. اگر نوسانی ندارید میتوانید گزینه no را بزنید   
 </details>
</div>

-------------------------------
  ![6348248](https://github.com/Azumi67/PrivateIP-Tunnel/assets/119934376/398f8b07-65be-472e-9821-631f7b70f783)
**آموزش مولتی سرور** 
- این اسکریپت بارها توسط من تست شده است. اگر اموزش کمی سخت بود بر روی سرور تست، آزمون و خطا کنید
- نمیتونستم اسکریپت رو ساده تر از این بکنم و با این حال احساس میکنم ممکن است کمی در نگاه اول، سخت باشد.
----------------

<div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش L2TP</summary>
  
  
------------------------------------ 

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/756f468e-8d6c-45bd-9a4a-a9d056011147)**سرور (خارج یا ایران) کانفیگ اول**

<p align="right">
  <img src="https://github.com/user-attachments/assets/a18e952d-7d44-4c0d-9daa-331d0af77ba9" alt="Image" />
</p>

- این یک نمونه کانفیگ برای روش L2TP میباشد. من در این مثال یک سرور خارج را توسط public ipv4 به دو کلاینت ایران متصل میکنم 
- برای هر کلاینت ایران به تعداد کانفیگ خارج اضافه میشود. به طور مثال اگر دو کلاینت ایران دارم پس دو کانفیگ سرور خارج هم خواهم داشت
- نکته ای که به ان باید توجه داشته باشد سرور میتواند سرور خارج یا ایران باشد و به همین منوال کلاینت میتواند خارج یا ایران باشد
- پس از نصب پیش نیاز ها، نخست از شما سوال میشود که ایپی پابلیک سرور را وارد نمایید و سپس ایپی پابلیک کلاینت را
- سپس ایپی اغازین ip range را وارد میکنم. مانند نمونه وارد نمایید. 192.168.1.0 و ایپی پایانی ip range 192.168.1.10
- سپس باید یک ایپی پرایوت برای l2tp وارد نمایید که من 192.168.1.1 را وارد میکنم
- پورت کانفیگ اول را 8000 میذارم
- مقدار mtu ها برای مثال است و من عدد 1410 را وارد میکنم
- سپس از من پرسیده میشود که ایا مایل به فعال ساری ipsec هستم یا خیر ؟ من بله را انتخاب میکنم و secret key را وارد مینمایم
- سپس از من پرسیده میشود که چند کلاینت دارم که من عدد 2 را انتخاب میکنم چون دو کلاینت دارم و ایپی های پابلیک انها را به نرنیب وارد میکنم

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/756f468e-8d6c-45bd-9a4a-a9d056011147)**سرور (خارج یا ایران) کانفیگ دوم**

<p align="right">
  <img src="https://github.com/user-attachments/assets/a0009220-da9c-4ecd-8d91-7745d9c0c48b" alt="Image" />
</p>

- کانفیگ دوم سرور را انجام میدهم
- ایپی پابلیک سرور را وارد نمایید و سپس ایپی پابلیک کلاینت را
- سپس باید یک ایپی پرایوت برای l2tp وارد نمایید که من 192.168.2.1 را وارد میکنم. چون کانفیگ دوم است قسمتی از پرایوت ایپی عوض میشود. کانفیگ اول 192.168.1.1 بود و کانفیگ دوم 192.168.2.1
- پورت کانفیگ دوم 8001 میذارم
- مقدار mtu ها برای مثال است و من عدد 1410 را وارد میکنم
- سپس از من پرسیده میشود که ایا مایل به فعال ساری ipsec هستم یا خیر ؟ من بله را انتخاب میکنم و secret key را وارد مینمایم
- سپس از من پرسیده میشود که چند کلاینت دارم که من عدد 2 را انتخاب میکنم چون دو کلاینت دارم و ایپی های پابلیک انها را به ترتیب وارد میکنم


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/756f468e-8d6c-45bd-9a4a-a9d056011147)**کلاینت ایران اول**

 <p align="right">
  <img src="https://github.com/user-attachments/assets/c3eeda20-3323-4c05-9ca0-495db4ba5f86" alt="Image" />
</p>

- ایپی پابلیک 4 کلاینت اول (ایران) را وارد میکنم و سپس ایپی پابلیک سرور (خارج) را وارد میکنم.
- ایپی اغاز و پایان برای ip range را مانند سرور وارد میکنم که به صورت 192.168.1.0 و 192.168.1.10 بود
- پرایوت ایپی برای کلاینت اول، ایپی مقابل سرور کانفیگ اول میباشد . ایپی سرور به این صورت بود 192.168.1.1 ، پس ایپی مقابل در کلاینت به صورت 192.168.1.2 میباشد
- پورت که 8000 بود و mtu هم بسته به نیاز خود وارد نمایید
- من ipsec را فعال میکنم و secret key را ازومی قرار میدهم

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/756f468e-8d6c-45bd-9a4a-a9d056011147)**کلاینت ایران دوم**

  <p align="right">
  <img src="https://github.com/user-attachments/assets/d46bba1c-3463-4324-b312-e679fd494ba8" alt="Image" />
</p>

- ایپی پابلیک 4 کلاینت دوم (ایران) را وارد میکنم و سپس ایپی پابلیک سرور (خارج) را وارد میکنم.
- ایپی اغاز و پایان برای ip range را یک عدد اضافه میکنم و به این صورت وارد میکنم. ایپی آغاز 192.168.2.0 و ایپی پایان 192.168.2.10
- پرایوت ایپی برای کلاینت دوم، ایپی مقابل سرور کانفیگ دوم میباشد . ایپی سرور به این صورت بود 192.168.2.1 ، پس ایپی مقابل در کلاینت به صورت 192.168.2.2 میباشد
- پورت کلاینت دوم که 8001 بود و mtu هم بسته به نیاز خود وارد نمایید
- من ipsec را فعال میکنم و secret key را ازومی قرار میدهم
 <p align="right">
  <img src="https://github.com/user-attachments/assets/cec38942-190a-4f1e-9d03-663401d87ff8" alt="Image" />
</p>

- توضیح کوتاهی برای edit l2tp میدم
- در اینجا میشود ایپی پابلیک ها و پرایوت ایپی های مربوطه و keepalive، پورت یا mtu را عوض کرد
- پس از انجام تغییرات گزینه save را بزنید.

-------------------
  </details>
</div>

<div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش eoip</summary>
  
  
------------------------------------ 

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/756f468e-8d6c-45bd-9a4a-a9d056011147)**سرور خارج**

<p align="right">
  <img src="https://github.com/user-attachments/assets/29cef5a3-8dcd-45fe-9836-5871484c2b10" alt="Image" />
</p>

- این یک نمونه کانفیگ برای روش EOIP میباشد. من در این مثال یک سرور خارج را توسط public ipv4 به دو کلاینت ایران متصل میکنم 
- نخست از من میپرسد که چند سرور ایران دارم. من دو عدد کلاینت ایران دارم پس عدد 2 را وارد میکنم.
- سپس public ipv4 سرور خارج را وارد میکنم. برای نمونه کانفیگ public ipv6، هم کانفیگ به همین صورت میباشد با این تفاوت که به جای public ipv4 از public ipv6 استفاده میکنید.
- سپس به ترتیب، ایپی های پابلیک 4 کلاینت های ایران را وارد میکنم. من دو عدد کلاینت دارم، پس باید به ترتیب کلاینت اول و دوم ایران را وارد کنم.
- سپس از من سوال میشود که private ip version باید بر اساس ایپی 4 یا ایپی 6 باشد. من ایپی 4 را انتخاب کردم.
- سپس برای هر کانفیگ یا پرایوت ایپی های هر کلاینت ، یک mtu متفاوت وارد میکنم.
- سپس از من سوال میشود که ایا میخواهم ipsec encryption انجام شود یا خیر. من گزینه y را میزنم و secret key را وارد میکنم
- سپس از من سوال میشود که ایا میخواهم ریست تایمر ipsec فعال شود یا خیر که گزینه y را وارد میکنم و عدد 2 دقیقه را انتخاب میکنم

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/756f468e-8d6c-45bd-9a4a-a9d056011147)**کلاینت ایران اول**

 <p align="right">
  <img src="https://github.com/user-attachments/assets/f36aae7b-aab0-4f02-ad1c-c85e95377580" alt="Image" />
</p>

- ایپی پابلیک 4 کلاینت اول ایران را وارد میکنم و سپس ایپی پابلیک خارج را وارد میکنم. ایپی پابلیک خارج در همه کلاینت ها یکسان میباشد
- سپس ورژن ایپی پرایوت را انتخاب میکنم. در سرور خارج ورژن ایپی پرایوت بر اساس ایپی 4 بود و در کلاینت ها هم باید بر اساس همین ورژن باشد
- پرایوت ایپی کانفیگ اول در سرور خارج 192.168.1.1 بود، پس در کلاینت اول ایپی پرایوت 192.168.1.2 خواهد بود
- در سرور خارج ipsec encryption فعال بود، پس باید در کلاینت ایران اول هم فعال باشد و secret key هم یکسان خواهد بود
- ریست تایمر هم که فعال و دو دقیقه بود

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/756f468e-8d6c-45bd-9a4a-a9d056011147)**کلاینت ایران دوم**

  <p align="right">
  <img src="https://github.com/user-attachments/assets/37261453-9bf1-425d-ad55-8791266b93c0" alt="Image" />
</p>

- ایپی پابلیک 4 کلاینت دوم ایران را وارد میکنم و سپس ایپی پابلیک خارج را وارد میکنم. ایپی پابلیک خارج در همه کلاینت ها یکسان میباشد
- سپس ورژن ایپی پرایوت را انتخاب میکنم. در سرور خارج ورژن ایپی پرایوت بر اساس ایپی 4 بود و در کلاینت ها هم باید بر اساس همین ورژن باشد
- پرایوت ایپی کانفیگ دوم در سرور خارج 176.10.10.1 بود، پس در کلاینت دوم، ایپی پرایوت 192.168.1.176.10.10.2 خواهد بود
- در سرور خارج ipsec encryption فعال بود، پس باید در کلاینت ایران دوم هم فعال باشد و secret key هم یکسان خواهد بود
- ریست تایمر هم که فعال و دو دقیقه بود
 <p align="right">
  <img src="https://github.com/user-attachments/assets/ba1508d3-fbc8-455f-ae1d-05e76795f61b" alt="Image" />
</p>

- توضیح کوتاهی برای edit local میدم
- در اینجا میشود ایپی پابلیک ها و پرایوت ایپی های مربوطه را عوض کرد
- پس از انجام تغییرات گزینه save را بزنید.

-------------------
  </details>
</div>
  
<div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش وایرگارد udp - دو کانفیگ خارج و دو کلاینت ایران</summary>
  
  
------------------------------------ 

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/756f468e-8d6c-45bd-9a4a-a9d056011147)**سرور خارج**

<p align="right">
  <img src="https://github.com/user-attachments/assets/184048c0-b66f-4635-9e95-37532b4a76d7" alt="Image" />
</p>

- این یک نمونه برای یادگیری شما میباشد و میشود پنج کانفیگ سرور و 5 کلاینت داشت. سرور میتواند خارج یا ایران باشد. اگر یک روش کار نکرد، روش دیگری را تست کنید.
- نخست توضیح مختصری از نحوه کانفیگ میدهم. من یک سرور خارج دارم و میخواهم از طریق وایرگارد این تانل را برقرار کنم. در سرور خارج به ازای هر کلاینت ایران، یک کانفیگ ایجاد میشود و برای همین نام ها در سرور خارج به این صورت ( سرور خارج کانفیگ اول و دوم ) میباشد که کانفیگ اول طبیعتا برای کلابنت اول ایران میباشد
- کلید های وایرگارد در سرور اصلی generate میشوند و از انها در کلاینت ها استفاده میشود. در هر کلاینت کلید پابلیک کانفیگ مربوطه و کلید پرایوت کلاینت ایران مربوطه وارد میشود. به طور مثال، در کلاینت ایران اول شما نیاز دارید که کلید پابلیک کانفیگ اول سرور خارج و کلید پرایوت کلاینت اول را وارد نمایید
- طبق عکس پیش میروم. من یک سرور خارج دارم و میخواهم به دو سرور ایران متصلش کنم. وارد گزینه 1 سرور خارج و 5 کلاینت ایران میشوم و گزینه 6 سرور خارج را انتخاب میکنم
- از من میپرسد که تعداد کلاینتهای ایران من چند عدد میباشد . من دو کلاینت ایران دارم پس عدد 2 را وارد میکنم
- سپس کانفیگ وایرگارد آغاز میشود و به من کلید های generate شده برای کانفیگ های سرور خارج و کلاینت های ایران نشان میدهد. این کلید ها بعدا در کلاینت ایران مربوطه استفاده میشود
  <p align="right">
  <img src="https://github.com/user-attachments/assets/be92ed52-7fbc-4321-b0a0-952e7ca91fcc" alt="Image" />
</p>

- حالا از من سوال میشود که ورژن ایپی خود را برای کانفیگ اول سرور خارج انتخاب نمایم. من میخواهم که پرایوت ایپی وایرگارد من بر اساس ایپی ورژن 4 باشد. پس گزینه 1 را انتخاب میکنم
- از بین ایپی های ورژن 4 یکی را انتخاب میکنم. شما میتوانید به صورت manual یک ایپی بدهید. اما باید دقت کنید که اگر به طور مثال ایپی پرایوت کانفیگ اول سرور خارج بدین صورت باشد 50.0.0.1، باید برای کلاینت ایپی مقابل را انتخاب نمایید که بدین صورت میشود : 50.0.0.2
- پورت تانل برای کانفیگ اول در سرور خارج را وارد میکنم. دقت نمایید برای هر کلاینت ایران یک پورت جداگانه وارد میکنید.
- سپس ایپی پابلیک 4 کلاینت اول ایران را وارد میکنم
- سپس از من میپرسد که پرایوت ایپی برای کلاینت اول به چه صورت باشد. ایپی 4 یا 6. چون من برای کانفیگ اول سرور خارج پرایوت ایپی 4 را انتخاب کرده بودم باید برای کلاینت هم همان ورژن را انتخاب کنم.
- مورد دیگر آنکه اگر به طور مثال 60.0.0.1 را برای کانفیگ اول سرور خارج وارد کردم، باید برای کلاینت ایپی مقابل را انتخاب کنم که میشود 60.0.0.2 . اگر این موارد رعایت نشود، وایرگارد برای شما کار نخواهد کرد. پس دقت کنید
- سپس از من سوال میشود که ایا میخواهم که اسکریپت خودش نام اینترفیس را پیدا کند که من گزینه y را میزنم که این کار انجام دهد.
  <p align="right">
  <img src="https://github.com/user-attachments/assets/42eec0a2-53ce-4777-8e0f-5a43a20f389d" alt="Image" />
</p>

- سپس از من سوال میشود که ایا میخواهم که برای کانفیگ اول سرور خارج (وایرگارد) MTU تنظیم کنم. شما میتوانید تنظیم کنید. من در این مثال از آن گذر میکنم.
- سپس وایرگارد up میشود.
  <p align="right">
  <img src="https://github.com/user-attachments/assets/27348510-6984-4d80-9dbd-60d64591d823" alt="Image" />
</p>

- چون دو کلاینت ایران دارم پس دو کانفیگ وایرگارد در سرور خارج دارم. پس کلید های مربوطه به کانفیگ دوم و کلاینت دوم ایران را نشان میدهد.
 <p align="right">
  <img src="https://github.com/user-attachments/assets/fb5265cb-9fb9-4047-aa53-b341579beb77" alt="Image" />
</p>

- مانند کانفیگ اول، ورژن پرایوت ایپی را انتخاب میکنم. من میخواهم پرایوت ایپی من بر اساس ایپی 4 باشد پس گزینه یک را انتخاب میکنم و یک پرایوت ایپی از لیست انتخاب میکنم
- پورت متفاوتی برای کلاینت دوم ایران وارد میکنم که اختلالی پیش نیاید.( دقت نمایید این پورت ها ربطی به کانفیگ های شما ندارد و برای ارتباط بین دو لوکال میباشد. به عبارتی این تانل تنها برای ارتباط بین دو سرور است و بعد از آن باید پورت فوروارد یا تانل اصلی را انجام دهید)
- حالا ایپی 4 پابلیک کلاینت دوم ایران را وارد میکنم
- سپس مانند قبل چون ورژن ایپی من برای کانفیگ دوم سرور خارج بر اساس 4 بوده است، همان ورژن و ایپی مقابلش را برای کلاینت دوم هم انتخاب میکنم
- سپس از من سوال میشود که ایا میخواهید نام اینترفیس را خود اسکریپت پیدا کند که من گزینه y را وارد میکنم
 <p align="right">
  <img src="https://github.com/user-attachments/assets/e0e7110c-6644-44f2-a077-0786d611959f" alt="Image" />
</p>

- سپس کانفیگ مربوطه وایرگارد up میشود و از شما سوال میشود که ایا IPSEC هم میخواهید یا خیر. در صورت انتخاب y ، باید secret key خود را وارد نمایید
- کانفیگ وایرگارد برای یک سرور خارج و دو کلاینت به پایان رسید
 <p align="right">
  <img src="https://github.com/user-attachments/assets/bdfccbc5-36cf-4141-9f75-12477a5c13dd" alt="Image" />
</p>

- توضیح کوتاهی برای edit local وایرگارد میدم
- ادرس که همان پرایوت ایپی کانفیگ اول سرور خارج میباشد
- مقدار Endpoint همان پابلیک ایپی کلاینت ایران میباشد
- مقدار allowed ip همان ایپی مقابل پرایوت ایپی میباشد.
- پورت هم که برای هر کانفیگ جداگانه است
- هر مقداری که را میخواهید تغییر بدهید، گزینه مربوطه را میزنید و سپس save n exit را انتخاب میکنید
 <p align="right">
  <img src="https://github.com/user-attachments/assets/448fea2c-9c7a-41e7-956a-ed800174aede" alt="Image" />
</p>

  - یک توضیح مختصر هم در مورد استاتوس وایرگارد میدهم. در این کانفیگ مربوطه تعداد دو کانفیگ، ایپی پابلیک هر کلاینت ، پورت هر کانفیگ . سایر موارد را نشان میدهد.
 ---------------------------------------
 
 ![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**کلاینت 
 ایران اول**


 <p align="right">
  <img src="https://github.com/user-attachments/assets/80870605-da68-4313-bacb-0a88aeaa8b6f" alt="Image" />
</p>

- کلاینت اول ایران را کانفیگ میکنم
- خب داخل سرور خارج برای هر کلاینت یک سری کلید هایی generate شده بود که در کلاینت ها باید وارد شوند. دقت نمایید که مقدار را درست وارد کنید وگرنه ممکن است تانل برای شما کار نکند
- از من سوال میشود که کلید پابلیک کانفیگ اول سرور خارج را وارد نمایم. این مقدار را در داخل سرور خارج پیدا میکنم و در اینجا paste مینمایم
- سپس سوال میشود که کلید پرایوت کلاینت اول ایران را وارد نمایم. این مقدار هم در سرور خارج generate شده بود و در اینجا paste میکنم
- سپس باید ایپی 4 پابلیک سرور خارج را وارد نمایم
- و پس از آن باید پورت کانفیگ اول سرور خارج را وارد نمایم که من مقدار 50820 را داده بودم
- سپس rule ها در فایروال اضافه میشود.
- من در سرور خارج برای کانفیگ اول از پرایوت ایپی ورژن 4 استفاده کرده بودم پس باید اینجا هم از ایپی ورژن 4 استفاده کنم.
- به طور مثال اگر من ایپی پرایوت 60.0.0.1 را برای کانفیگ اول سرور خارج وارد کرده بودم پس همیشه برای کلاینت، ایپی مقابل این مقدار را وارد میکنم که میشود 60.0.0.2
- پس ایپی پرایوت کلاینت اول را انتخاب میکنم
 <p align="right">
  <img src="https://github.com/user-attachments/assets/90e0ab6a-d620-49c9-bcad-980864246099" alt="Image" />
</p>

- سپس ایپی پرایوتی که برای کانفیگ اول خارج داده بودیم را دوباره انتخاب میکنم
- از من سوال میشود که ایا میخواهم اینترفیس به صورت اتوماتیک توسط اسکریپت پیدا شود که گزینه y را میزنم
- از تنظیم mtu برای وایرگارد هم گذر میکنم
- سپس وایرگارد up میشود
- اگر در سرور خارج ipsec را کانفیگ کردید در کلاینت ها هم باید کانفیک نمایید . در صورت کانفیگ باید secret key سرور خارج را در کلاینت هم وارد نمایید.
---------------------------------------
 
 ![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**کلاینت 
 ایران دوم**

 <p align="right">
  <img src="https://github.com/user-attachments/assets/2b3cfdc2-c455-4114-90b4-b8570042fd71" alt="Image" />
</p>

- کلاینت دوم ایران را کانفیگ میکنم
- از من سوال میشود که کلید پابلیک کانفیگ دوم سرور خارج را وارد نمایم. این مقدار را در داخل سرور خارج پیدا میکنم و در اینجا paste مینمایم
- سپس سوال میشود که کلید پرایوت کلاینت دوم ایران را وارد نمایم. این مقدار هم در سرور خارج generate شده بود و در اینجا paste میکنم
- سپس باید ایپی 4 پابلیک سرور خارج را وارد نمایم
- و پس از آن باید پورت کانفیگ دوم سرور خارج را وارد نمایم که من مقدار 50821 را داده بودم
- سپس rule ها در فایروال اضافه میشود.
- من در سرور خارج برای کانفیگ دوم از پرایوت ایپی ورژن 4 استفاده کرده بودم پس باید اینجا هم از ایپی ورژن 4 استفاده کنم.
- به طور مثال اگر من ایپی پرایوت 60.1.0.1 را برای کانفیگ دوم سرور خارج وارد کرده بودم پس همیشه برای کلاینت، ایپی مقابل این مقدار را وارد میکنم که میشود 60.1.0.2
- پس ایپی پرایوت کلاینت دوم را انتخاب میکنم
 <p align="right">
  <img src="https://github.com/user-attachments/assets/45f8f3b7-3e13-425d-acbc-a75df26d0ae7" alt="Image" />
</p>

- سپس ایپی پرایوتی که برای کانفیگ دوم خارج داده بودیم را دوباره انتخاب میکنم
- از من سوال میشود که ایا میخواهم اینترفیس به صورت اتوماتیک توسط اسکریپت پیدا شود که گزینه y را میزنم
- از تنظیم mtu برای وایرگارد هم گذر میکنم
- سپس وایرگارد up میشود
- اگر در سرور خارج ipsec را کانفیگ کردید در کلاینت ها هم باید کانفیک نمایید . در صورت کانفیگ باید secret key سرور خارج را در کلاینت هم وارد نمایید.


-------------------
  </details>
</div>
<div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش sit به همراه وایرگارد - یک کانفیگ سرور خارج و یک کلاینت ایران</summary>
  
  
------------------------------------ 

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/756f468e-8d6c-45bd-9a4a-a9d056011147)**سرور خارج**

<p align="right">
  <img src="https://github.com/user-attachments/assets/2f85e144-70ec-4fc6-9091-6a84046bcde0" alt="Image" />
</p>

- این یک نمونه برای یادگیری شما میباشد و میشود پنج کانفیگ سرور و 5 کلاینت داشت. سرور میتواند خارج یا ایران باشد. اگر یک روش کار نکرد، روش دیگری را تست کنید.
- نخست توضیح مختصری از نحوه کانفیگ میدهم. من یک سرور خارج دارم و میخواهم از طریق sit و وایرگارد این تانل را برقرار کنم. در سرور خارج به ازای هر کلاینت ایران، یک کانفیگ ایجاد میشود و برای همین نام ها در سرور خارج به این صورت ( سرور خارج کانفیگ اول و دوم ) میباشد که کانفیگ اول طبیعتا برای کلابنت اول ایران میباشد
- کلید های وایرگارد در سرور اصلی generate میشوند و از انها در کلاینت ها استفاده میشود. در هر کلاینت کلید پابلیک کانفیگ مربوطه و کلید پرایوت کلاینت ایران مربوطه وارد میشود. به طور مثال، در کلاینت ایران اول شما نیاز دارید که کلید پابلیک کانفیگ اول سرور خارج و کلید پرایوت کلاینت اول را وارد نمایید
- طبق عکس پیش میروم. من یک سرور خارج دارم و میخواهم به یک کلاینت ایران متصلش کنم. وارد گزینه 1 سرور خارج و 5 کلاینت ایران میشوم و گزینه 6 سرور خارج را انتخاب میکنم
- از من میپرسد که تعداد کلاینتهای ایران من چند عدد میباشد . من یک کلاینت ایران دارم پس عدد 1 را وارد میکنم
- سپس کانفیگ sit اغاز میشود و ایپی پابلیک 4 ایران و خارج را وارد میکنم و از تنظیم mtu گذر میکنم
<p align="right">
  <img src="https://github.com/user-attachments/assets/cb715802-ca95-4a2e-b5ab-3d0ceb8dafa0" alt="Image" />
</p>
- سپس کانفیگ وایرگارد آغاز میشود و به من کلید های generate شده برای کانفیگ های سرور خارج و کلاینت های ایران را نشان میدهد. این کلید ها بعدا در کلاینت ایران مربوطه استفاده میشود
  <p align="right">
  <img src="https://github.com/user-attachments/assets/fb4e702b-35c1-45cc-bcf2-97db4f8e4438" alt="Image" />
</p>

- حالا از من سوال میشود که ورژن ایپی خود را برای کانفیگ اول سرور خارج انتخاب نمایم. من میخواهم که پرایوت ایپی وایرگارد من بر اساس ایپی ورژن 6 باشد. پس گزینه 2 را انتخاب میکنم
- از بین ایپی های ورژن 6 یکی را انتخاب میکنم. شما میتوانید به صورت manual یک ایپی بدهید. اما باید دقت کنید که اگر به طور مثال ایپی پرایوت کانفیگ اول سرور خارج بدین صورت باشد 1::2001 ، باید برای کلاینت ایپی مقابل را انتخاب نمایید که بدین صورت میشود 2::2001
- پورت تانل برای کانفیگ اول در سرور خارج را وارد میکنم. دقت نمایید برای هر کلاینت ایران یک پورت جداگانه وارد میکنید.
- سپس از من میپرسد که پرایوت ایپی برای کلاینت اول به چه صورت باشد. ایپی 4 یا 6. چون من برای کانفیگ اول سرور خارج پرایوت ایپی 6 را انتخاب کرده بودم باید برای کلاینت هم همان ورژن را انتخاب کنم.
- مورد دیگر آنکه اگر به طور مثال 1::2001 را برای کانفیگ اول سرور خارج وارد کردم، باید برای کلاینت ایپی مقابل را انتخاب کنم که میشود 2::2001 . اگر این موارد رعایت نشود، وایرگارد برای شما کار نخواهد کرد. پس دقت کنید
- سپس از من سوال میشود که ایا میخواهم که اسکریپت خودش نام اینترفیس را پیدا کند که من گزینه y را میزنم که این کار انجام دهد.
- سپس از من سوال میشود که ایا میخواهم که برای کانفیگ اول سرور خارج (وایرگارد) MTU تنظیم کنم. شما میتوانید تنظیم کنید. من در این مثال از آن گذر میکنم.
- سپس وایرگارد up میشود.
 
 ---------------------------------------
 
 ![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**کلاینت 
 ایران اول**

 <p align="right">
  <img src="https://github.com/user-attachments/assets/fad8baa1-3900-4b92-9fad-1d57a2a3a69d" alt="Image" />
</p>

- کلاینت اول ایران را کانفیگ میکنم
- کانفیگ sit اغاز میشود و ایپی پابلیک 4 ایران و خارج را وارد میکنم و از تنظیم mtu گذر میکنم
 <p align="right">
  <img src="https://github.com/user-attachments/assets/3cb350a0-82c6-4c76-8016-fc1fafafbca6" alt="Image" />
</p> 

- خب داخل سرور خارج برای هر کلاینت یک سری کلید هایی generate شده بود که در کلاینت ها باید وارد شوند. دقت نمایید که مقدار را درست وارد کنید وگرنه ممکن است تانل برای شما کار نکند
- از من سوال میشود که کلید پابلیک کانفیگ اول سرور خارج را وارد نمایم. این مقدار را در داخل سرور خارج پیدا میکنم و در اینجا paste مینمایم
- سپس سوال میشود که کلید پرایوت کلاینت اول ایران را وارد نمایم. این مقدار هم در سرور خارج generate شده بود و در اینجا paste میکنم
- و پس از آن باید پورت کانفیگ اول سرور خارج را وارد نمایم که من مقدار 50820 را داده بودم
- سپس rule ها در فایروال اضافه میشود.
- من در سرور خارج برای کانفیگ اول از پرایوت ایپی ورژن 6 استفاده کرده بودم پس باید اینجا هم از ایپی ورژن 6 استفاده کنم.
- به طور مثال اگر من ایپی پرایوت 1::2001 را برای کانفیگ اول سرور خارج وارد کرده بودم پس همیشه برای کلاینت، ایپی مقابل این مقدار را وارد میکنم که میشود 2::2001
- پس ایپی پرایوت کلاینت اول را انتخاب میکنم و سپس ایپی پرایوت کانفیگ اول سرور خارج
 <p align="right">
  <img src="https://github.com/user-attachments/assets/3768b112-f9dd-4387-a1b3-ca98cc662a5f" alt="Image" />
</p>

- از من سوال میشود که ایا میخواهم اینترفیس به صورت اتوماتیک توسط اسکریپت پیدا شود که گزینه y را میزنم
- از تنظیم mtu برای وایرگارد هم گذر میکنم
- سپس وایرگارد up میشود
- اگر در سرور خارج ipsec را کانفیگ کردید در کلاینت ها هم باید کانفیک نمایید . در صورت کانفیگ باید secret key سرور خارج را در کلاینت هم وارد نمایید.
 <p align="right">
  <img src="https://github.com/user-attachments/assets/5caa439b-4d67-4e18-ae14-0d481b255a4f" alt="Image" />
</p>

- توضیج کوتاهی در باب edit local این روش هم میدهم.
- ایپی پابلیک sit برای اتصال بین دو سرور کلاینت است و در صورت عوض شدن کلاینت و سرور، قابلیت تغییر دارد
- پرایوت ایپی sit، مقدار endpoint وایرگارد را عوض میکند
- ادرس یا پرایوت ایپی وایرگارد هم برای ایپی پرایوت نهایی استفاده میشود

-------------------
  </details>
</div>
<div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش native gre6tap و وایرگارد - یک کانفیگ سرور ایران و یک کلاینت خارج</summary>
  
  
------------------------------------ 

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/756f468e-8d6c-45bd-9a4a-a9d056011147)**سرور ایران**

<p align="right">
  <img src="https://github.com/user-attachments/assets/18aa3b0c-dd02-49ec-b580-81d5746c46b9" alt="Image" />
</p>

- این یک نمونه برای یادگیری شما میباشد و میشود پنج کانفیگ سرور و 5 کلاینت داشت. سرور میتواند خارج یا ایران باشد. اگر یک روش کار نکرد، روش دیگری را تست کنید.
- نخست توضیح مختصری از نحوه کانفیگ میدهم. من یک سرور ایران دارم و میخواهم از طریق ایپی 6 ایران و خارج و هم چنین وایرگارد این تانل را برقرار کنم. در سرور ایران به ازای هر کلاینت ایران، یک کانفیگ ایجاد میشود و برای همین نام ها در سرور ایران به این صورت ( سرور ایران کانفیگ اول و دوم ) میباشد که کانفیگ اول طبیعتا برای کلابنت اول خارج میباشد
- کلید های وایرگارد در سرور اصلی generate میشوند و از انها در کلاینت ها استفاده میشود. در هر کلاینت کلید پابلیک کانفیگ مربوطه و کلید پرایوت کلاینت خارج مربوطه وارد میشود. به طور مثال، در کلاینت خارج اول شما نیاز دارید که کلید پابلیک کانفیگ اول سرور ایران و  کلید پرایوت کلاینت اول را وارد نمایید
- طبق عکس پیش میروم. من یک سرور ایران دارم و میخواهم به یک کلاینت خارج متصلش کنم. وارد گزینه 1 سرور ایران و 5 کلاینت خارج میشوم و گزینه 6 سرور ایران را انتخاب میکنم
- از من میپرسد که تعداد کلاینتهای خارج من چند عدد میباشد . من یک کلاینت  دارم پس عدد 1 را وارد میکنم
- سپس کانفیگ native gre6tap اغاز میشود و باید ایپی پابلیک 6 سرور ایران و کلاینت خارج را وارد نمایم .
- سپس باید مشخص کنم که ایا میخواهم mtu را به صورت manual وارد نمایم یا خیر
<p align="right">
  <img src="https://github.com/user-attachments/assets/ff2662d5-18ea-4545-8b81-b3aad88f11f0" alt="Image" />
</p>
- سپس کانفیگ وایرگارد آغاز میشود و به من کلید های generate شده برای کانفیگ های سرور ایران و کلاینت های خارج را نشان میدهد. این کلید ها بعدا در کلاینت خارج مربوطه استفاده میشود
  <p align="right">
  <img src="https://github.com/user-attachments/assets/d26fbf5b-6787-4f43-a6c0-e6a00df94ae8" alt="Image" />
</p>

- حالا از من سوال میشود که ورژن ایپی خود را برای کانفیگ اول سرور ایران انتخاب نمایم. من میخواهم که پرایوت ایپی وایرگارد من بر اساس ایپی ورژن 4 باشد. پس گزینه 1 را انتخاب میکنم
- از بین ایپی های ورژن 4 یکی را انتخاب میکنم. شما میتوانید به صورت manual یک ایپی بدهید. اما باید دقت کنید که اگر به طور مثال ایپی پرایوت کانفیگ اول سرور ایران بدین صورت باشد 50.0.0.1، باید برای کلاینت ایپی مقابل را انتخاب نمایید که بدین صورت میشود : 50.0.0.2
- پورت تانل برای کانفیگ اول در سرور ایران را وارد میکنم. دقت نمایید برای هر کلاینت خارج یک پورت جداگانه وارد میکنید.
- دیگر نیازی به وارد کردن پابلیک ایپی نمیباشد از انجا که پرایوت ایپی در این روش به جای public ip استفاده میشود 
- سپس از من میپرسد که پرایوت ایپی برای کلاینت اول به چه صورت باشد. ایپی 4 یا 6. چون من برای کانفیگ اول سرور ایران پرایوت ایپی 4 را انتخاب کرده بودم باید برای کلاینت هم همان ورژن را انتخاب کنم.
- مورد دیگر آنکه اگر به طور مثال 60.0.0.1 را برای کانفیگ اول سرور ایران وارد کردم، باید برای کلاینت ایپی مقابل را انتخاب کنم که میشود 60.0.0.2 . اگر این موارد رعایت نشود، وایرگارد برای شما کار نخواهد کرد. پس دقت کنید
- سپس از من سوال میشود که ایا میخواهم که اسکریپت خودش نام اینترفیس را پیدا کند که من گزینه y را میزنم که این کار انجام دهد.
- سپس از من سوال میشود که ایا میخواهم که برای کانفیگ اول سرور خارج (وایرگارد) MTU تنظیم کنم. شما میتوانید تنظیم کنید. من در این مثال از آن گذر میکنم.
- سپس وایرگارد up میشود.
- سپس از شما سوال میشود که ایا ipsec را میخواهید کانفیگ کنید که در صورت کانفیگ باید secret key مورد تمایل خود را وارد نمایید

 ---------------------------------------
 
 ![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**کلاینت 
 خارج اول**

 <p align="right">
  <img src="https://github.com/user-attachments/assets/13158994-b9be-4720-a087-8ae14ccd6415" alt="Image" />
</p>

- کلاینت اول خارج را کانفیگ میکنم
- نخست از ما برای کانفیگ gre6tap سوال میشود که ایپی 6 کلاینت اول خارج و ایپی 6 سرور ایران را وارد میکنم
- از تنظیم mtu هم گذر میکنم و سپس تلاش میشود که بین دو سرور و کلاینت، اتصال پینگ تست شود
 <p align="right">
  <img src="https://github.com/user-attachments/assets/03e87777-84a0-4722-a75a-ad6606be594c" alt="Image" />
</p>

- خب داخل سرور ایران برای هر کلاینت یک سری کلید هایی generate شده بود که در کلاینت ها باید وارد شوند. دقت نمایید که مقدار را درست وارد کنید وگرنه ممکن است تانل برای شما کار نکند
- از من سوال میشود که کلید پابلیک کانفیگ اول سرور ایران را وارد نمایم. این مقدار را در داخل سرور ایران پیدا میکنم و در اینجا paste مینمایم
- سپس سوال میشود که کلید پرایوت کلاینت اول خارج را وارد نمایم. این مقدار هم در سرور ایران generate شده بود و در اینجا paste میکنم
- و پس از آن باید پورت کانفیگ اول سرور ایران را وارد نمایم که من مقدار 50820 را داده بودم
- سپس rule ها در فایروال اضافه میشود.
 <p align="right">
  <img src="https://github.com/user-attachments/assets/04f26140-1fab-43f5-b56c-5a34891731be" alt="Image" />
</p>

- من در سرور ایران برای کانفیگ اول از پرایوت ایپی ورژن 4 استفاده کرده بودم پس باید اینجا هم از ایپی ورژن 4 استفاده کنم.
- به طور مثال اگر من ایپی پرایوت 60.0.0.1 را برای کانفیگ اول سرور ایران وارد کرده بودم پس همیشه برای کلاینت، ایپی مقابل این مقدار را وارد میکنم که میشود 60.0.0.2
- پس ایپی پرایوت کلاینت اول را انتخاب میکنم که در این لیست 60.2.0.2 میباشد و برای کانفیگ اول سرور ایران هم 60.2.0.1 را وارد میکنم
 <p align="right">
  <img src="https://github.com/user-attachments/assets/fef029fc-61e7-4c40-87e9-2d5e7803c78b" alt="Image" />
</p>

- از من سوال میشود که ایا میخواهم اینترفیس به صورت اتوماتیک توسط اسکریپت پیدا شود که گزینه y را میزنم
- از تنظیم mtu برای وایرگارد هم گذر میکنم
- سپس وایرگارد up میشود
- اگر در سرور ایران ipsec را کانفیگ کردید در کلاینت ها هم باید کانفیک نمایید . در صورت کانفیگ باید secret key سرور ایران را در کلاینت هم وارد نمایید.

-------------------
  </details>
</div>

<div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش وایرگارد و gre6tap - دو کانفیگ ایران و دو کلاینت خارج</summary>
  
  
------------------------------------ 

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/756f468e-8d6c-45bd-9a4a-a9d056011147)**سرور خارج**

<p align="right">
  <img src="https://github.com/user-attachments/assets/d5f8fa39-448e-4731-9708-fb9c35e8427b" alt="Image" />
</p>

-- این یک نمونه برای یادگیری شما میباشد و میشود پنج کانفیگ سرور و 5 کلاینت داشت. سرور میتواند خارج یا ایران باشد. اگر یک روش کار نکرد، روش دیگری را تست کنید.
- نخست توضیح مختصری از نحوه کانفیگ میدهم. من یک سرور ایران دارم و میخواهم از طریق وایرگارد این تانل را برقرار کنم. در سرور ایران به ازای هر کلاینت خارج، یک کانفیگ ایجاد میشود و برای همین نام ها در سرور ایران به این صورت ( سرور ایران کانفیگ اول و دوم ) میباشد که کانفیگ اول طبیعتا برای کلابنت اول خارج میباشد
- کلید های وایرگارد در سرور اصلی generate میشوند و از انها در کلاینت ها استفاده میشود. در هر کلاینت کلید پابلیک کانفیگ مربوطه و کلید پرایوت کلاینت ایران مربوطه وارد میشود. به طور مثال، در کلاینت خارج اول شما نیاز دارید که کلید پابلیک کانفیگ اول سرور ایران و کلید پرایوت کلاینت اول را وارد نمایید
- طبق عکس پیش میروم. من یک سرور ایران دارم و میخواهم به دو سرور خارج متصلش کنم. وارد گزینه 1 سرور ایران و 5 کلاینت خارج میشوم و گزینه 6 سرور ایران را انتخاب میکنم
- از من میپرسد که تعداد کلاینتهای خارج من چند عدد میباشد . من دو کلاینت خارج دارم پس عدد 2 را وارد میکنم
- سپس کانفیگ وایرگارد آغاز میشود و به من کلید های generate شده برای کانفیگ های سرور ایران و کلاینت های خارج را نشان میدهد. این کلید ها بعدا در کلاینت خارج مربوطه استفاده میشود
  <p align="right">
  <img src="https://github.com/user-attachments/assets/90a019ac-ceb6-4402-b74a-526e9157907a" alt="Image" />
</p>

- در این روش تنها از ایپی ورژن 6 میتوان استفاده کرد
- از بین ایپی های ورژن 6 یکی را انتخاب میکنم. شما میتوانید به صورت manual یک ایپی بدهید. اما باید دقت کنید که اگر به طور مثال ایپی پرایوت کانفیگ اول سرور ایران بدین صورت باشد 1::2001، باید برای کلاینت ایپی مقابل را انتخاب نمایید که بدین صورت میشود : 2::2001
- پورت تانل برای کانفیگ اول در سرور ایران را وارد میکنم. دقت نمایید برای هر کلاینت خارج یک پورت جداگانه وارد میکنید.
- سپس ایپی پابلیک 4 کلاینت اول خارج را وارد میکنم
- سپس ایپی پرایوت 6 برای کلاینت را از داخل لیست انتخاب میکنم ( شما میتوانید حتی به صورت manual وارد نمایید)
- سپس از من سوال میشود که ایا میخواهم که اسکریپت خودش نام اینترفیس را پیدا کند که من گزینه y را میزنم که این کار انجام دهد.
- سپس از من سوال میشود که ایا میخواهم که برای کانفیگ اول سرور خارج (وایرگارد) MTU تنظیم کنم. شما میتوانید تنظیم کنید. من در این مثال از آن گذر میکنم.
- سپس وایرگارد up میشود.
  <p align="right">
  <img src="https://github.com/user-attachments/assets/beca6fbb-18ce-4a15-b21a-b670929340c6" alt="Image" />
</p>

- چون دو کلاینت خارج دارم پس دو کانفیگ وایرگارد در سرور ایران دارم. پس کلید های مربوطه به کانفیگ دوم و کلاینت دوم خارج را نشان میدهد.
- مانند کانفیگ اول، ایپی پرایوت مناسب برای کلاینت دوم را انتخاب میکنم . باید ایپی مقابل پرایوت ایپی کانفیگ دوم سرور خارج باشد . اگر مثلا ایپی کانفیگ دوم 1::2001 است باید برای کلاینت 2::2001 را انتخاب کنم 
- پورت متفاوتی برای کلاینت دوم خارج وارد میکنم که اختلالی پیش نیاید.( دقت نمایید این پورت ها ربطی به کانفیگ های شما ندارد و برای ارتباط بین دو لوکال میباشد. به عبارتی این تانل تنها برای ارتباط بین دو سرور است و بعد از آن باید پورت فوروارد یا تانل اصلی را انجام دهید)
- حالا ایپی 4 پابلیک کلاینت دوم خارج را وارد میکنم
 <p align="right">
  <img src="https://github.com/user-attachments/assets/ea7b2fa4-0c93-48aa-8132-0a746f4d4030" alt="Image" />
</p>

- سپس از من سوال میشود که ایا میخواهید نام اینترفیس را خود اسکریپت پیدا کند که من گزینه y را وارد میکنم
- سپس کانفیگ های gre6tap اغاز میشود که تنها نیاز است که مشخص کنید ایا میخواهید gre6tap mtu را به صورت manual وارد کنید یا خیر
- چون دو کلاینت خارج داریم پس دو بار کانفیگ gre6tap انجام میشود.
 <p align="right">
  <img src="https://github.com/user-attachments/assets/1bfa0b07-f042-4395-a96d-09ac6a9aa244" alt="Image" />
</p>

- تلاشی برای گرفتن پینگ بین دو سرور و کلاینت صورت میگیرد.
- پس از ان از من سوال میشود که ایا میخوام ipsec را کانفیگ کنم یا خیر که در صورت کانفیگ باید یک secret key هم مشخص کنید.
 ---------------------------------------
 
 ![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**کلاینت 
 خارج اول**


 <p align="right">
  <img src="https://github.com/user-attachments/assets/13436c99-b151-4487-b01b-c64dd7d1cb86" alt="Image" />
</p>

- کلاینت اول خارج را کانفیگ میکنم
- خب داخل سرور ایران برای هر کلاینت یک سری کلید هایی generate شده بود که در کلاینت ها باید وارد شوند. دقت نمایید که مقدار را درست وارد کنید وگرنه ممکن است تانل برای شما کار نکند
- از من سوال میشود که کلید پابلیک کانفیگ اول سرور ایران را وارد نمایم. این مقدار را در داخل سرور ایران پیدا میکنم و در اینجا paste مینمایم
- سپس سوال میشود که کلید پرایوت کلاینت اول خارج را وارد نمایم. این مقدار هم در سرور ایران generate شده بود و در اینجا paste میکنم
- سپس باید ایپی 4 پابلیک سرور ایران را وارد نمایم
- و پس از آن باید پورت کانفیگ اول سرور ایران را وارد نمایم که من مقدار 50820 را داده بودم
- سپس rule ها در فایروال اضافه میشود.
- من در سرور ایران برای کانفیگ اول از پرایوت ایپی ورژن 6 استفاده کرده بودم پس باید اینجا هم از ایپی ورژن 6 استفاده کنم.
- پس ایپی پرایوت کلاینت اول را انتخاب میکنم
- سپس ایپی پرایوتی که برای کانفیگ اول سرور ایران داده بودم را دوباره انتخاب میکنم
- از من سوال میشود که ایا میخواهم اینترفیس به صورت اتوماتیک توسط اسکریپت پیدا شود که گزینه y را میزنم
- از تنظیم mtu برای وایرگارد هم گذر میکنم
- سپس وایرگارد up میشود
- اگر در سرور خارج ipsec را کانفیگ کردید در کلاینت ها هم باید کانفیک نمایید . در صورت کانفیگ باید secret key سرور ایران را در کلاینت هم وارد نمایید.
---------------------------------------
 
 ![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/49000de2-53b6-4c5c-888d-f1f397d77b92)**کلاینت 
 خارج دوم**
 <p align="right">
  <img src="https://github.com/user-attachments/assets/05dc9e6f-e192-4ae9-aa16-ad98136a0f92" alt="Image" />
</p>

- کلاینت دوم خارج را کانفیگ میکنم
- از من سوال میشود که کلید پابلیک کانفیگ دوم سرور ایران را وارد نمایم. این مقدار را در داخل سرور ایران پیدا میکنم و در اینجا paste مینمایم
- سپس سوال میشود که کلید پرایوت کلاینت دوم خارج را وارد نمایم. این مقدار هم در سرور ایران generate شده بود و در اینجا paste میکنم
- سپس باید ایپی 4 پابلیک سرور ایران را وارد نمایم
- و پس از آن باید پورت کانفیگ دوم سرور ایران را وارد نمایم که من مقدار 50821 را داده بودم
- سپس rule ها در فایروال اضافه میشود.
- من در سرور ایران برای کانفیگ دوم از پرایوت ایپی ورژن 6 استفاده کرده بودم پس باید اینجا هم از ایپی ورژن 6 استفاده کنم.
- پس ایپی پرایوت کلاینت دوم را انتخاب میکنم
- سپس ایپی پرایوتی که برای کانفیگ دوم سرور ایران داده بودم را دوباره انتخاب میکنم
- از من سوال میشود که ایا میخواهم اینترفیس به صورت اتوماتیک توسط اسکریپت پیدا شود که گزینه y را میزنم
- از تنظیم mtu برای وایرگارد هم گذر میکنم
- سپس وایرگارد up میشود
- اگر در سرور ایران ipsec را کانفیگ کردید در کلاینت ها هم باید کانفیک نمایید . در صورت کانفیگ باید secret key سرور ایران را در کلاینت هم وارد نمایید.
  
 <p align="right">
  <img src="https://github.com/user-attachments/assets/a9ddf952-5b2c-459f-98f4-679883be0a9d" alt="Image" />
</p>

- در این اسکرین ادرس همان پرایوت ایپی وایرگارد است و ایپی مقابل ان ALLOWED IP است. ایپی وایرگارد برای LOCAL & REMOTE در GRE6TAP هم استفاده میشود
- پورت که برای هر کانفیگ متفاوت میباشد
- مقدار Endpoint هم همان پابلیک ایپی کلاینت میباشد
- پرایوت ایپی gre6tap هم به صورت جداکانه میتوان تغییر داد.
- گس از تغییر save n exit را انتخاب نمایید

-------------------
  </details>
</div>
  </details>
</div>  
<div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش ISATAP یک سرور خارج و دو کلاینت ایران</summary>

---------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور خارج**



<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/d133cd7e-05c7-4fcd-98f2-9142738b0875" alt="Image" />
</p>

- تمام تلاشم را کرده ام که در این روش، شما نیاز نباشد که به صورت manual پرفیکس هایی که ایجاد میشود را در سرور اصلی وارد کنید چون نیاز بود که در هنگام کانفیگ بین سرور و کلاینت در گردش باشید. بنابراین در حال حاضر باید نخست سرور خارج را کانفیگ کرد و سپس کلاینت های ایران را کانفیگ کرد
- مورد دیگری که هست در اینجا من سرور را خارج در نظر میگیرم و کلاینت را ایران. میتوان سرور را ایران در نظر گرفت و کلاینت ها خارج باشد که در اموزش دیگری قرار خواهم داد
- هم چنین در این روش از ریست لوکال استفاده میکنم که به صورت تست میباشد و در صورت استفاده میتوانید کارایی این مورد را با من در میان بگذارید.
- اگر این روش کارکرد خوبی داشت، 5 سرور و 5 کلاینت هم اضافه میکنم
- خب من 1 سرور خارج و 2 کلاینت ایران دارم.
- نخست ایپی 4 سرور خارج را وارد میکنم
- از من پرسیده میشود که mtu را به صورت manual وارد میکنید یا خیر. من n را وارد میکنم
- ایپی پرایوت شما نمایش داده میشود و سپس از من سوال میشود که چه تعداد کلاینت ایران دارم. من دو عدد کلاینت ایران دارم پس عدد 2 را وارد میکنم.
- ایپی 4 کلاینت اول ایران و پورت مورد نظر را وارد میکنم ( برای هر کلاینت باید پورت متفاوتی بدهید و ufw این پورت را به فایروال اضافه میکند)
- ایپی 4 کلاینت دوم ایران و پورت مورد نظر را وارد میکنم
- اگر از ufw استفاده میکنید بهتر است قبل از انجام کانفیگ، آن را disable کنید و سپس enable کنید یا ufw reload
- نخست از من سوال میشود که چند سرور ایران دارم. من دو سرور ایران دارم پس عدد 2 را وارد میکنم.
- سپس از من سوال میشود که ایا IPSEC فعال شود که من y را وارد میکنم و سپس secret key را azumi وارد میکنم ( شما میتوانید پیچیده تر بذارید)

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/84c50c16-e0f7-4af3-9df2-f19937ed2bad" alt="Image" />
</p>

- سپس از من میپرسد که ریست تایمر IPSEC بر چه اساس و unit ای باشد. من دقیقه را وارد میکنم و عدد 2 را وارد میکنم. مقدار شما میتواند متفاوت باشد
- سپس از من سوال میشود که ایا میخواهم لوکال من بر اساس زمانی خاص ریست شود که برای تست من گزینه y را وارد میکنم و به طور مثال هر ساعت میخواهم که این ریست انجام شود
- دقت نمایید شما میتوانید گزینه n را وارد کنید و ریست تایمر لوکال را فعال نکنید.
- اگر خطای بافر سایز گرفتید لطفا اطمینان حاصل فرمایید که روش های قبلی که در تضاد است ، پاک کرده باشید.
- از طریق گزینه Status میتوانید از فعال بودن روش و ایپی های کلاینت و سایر موارد آگاه شوید.

---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **کلاینت ایران اول**

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/ae812ca8-95f2-4eb6-bb89-c24f96683738" alt="Image" />
</p>

- کلاینت ایران اول را کانفیگ میکنم.
- ایپی 4 کلاینت اول ایران را وارد میکنم
- سپس ایپی 4 سرور را وارد میکنم و به صورت اتومات prefix سرور خارج در کلاینت اضافه میشود.
- پورتی که برای کلاینت ایران اول را وارد کرده بودم را اینجا وارد میکنم که 5050 بود
- از من سوال میشود که mtu را manual وارد کنم که n را میزنم تا اتومات انتخاب شود.
- ایپی پرایوت این کلاینت نمایش داده میشود و سپس از من سوال میشود که آیا IPSEC فعال شود یا خیر که من y را وارد میکنم تا فعال شود
- سپس از من سوال میشود که ریست تایمر IPSEC چه باشد که من 2 دقیقه قرار میدهم. شما میتوانید مقدار دیگری قرار دهید

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/99125f0b-470f-4dad-b5e2-bf1bc5a03828" alt="Image" />
</p>

- سپس از من سوال میشود که ایا میخواهم لوکال تانل من بر اساس بازه زمانی خاصی، ریست شود که من y را وارد میکنم و مقدار یک ساعت را وارد میکنم. شما میتوانید n بزنید که غیرفعال شود یا مقدار دیگری برای زمان انتخاب نمایید.(این عدد ها قابل تغییر است و فقط برای نمونه استفاده شده است)

---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **کلاینت ایران دوم**

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/e872f99d-88a3-4304-8106-94e981291aa9" alt="Image" />
</p>

- کلاینت ایران دوم را کانفیگ میکنم.
- ایپی 4 کلاینت دوم ایران را وارد میکنم
- سپس ایپی 4 سرور را وارد میکنم و به صورت اتومات prefix سرور خارج در کلاینت دوم اضافه میشود.
- پورتی که برای کلاینت ایران دوم را وارد کرده بودم را اینجا وارد میکنم که 5051 بود
- از من سوال میشود که mtu را manual وارد کنم که n را میزنم تا اتومات انتخاب شود.
- ایپی پرایوت این کلاینت نمایش داده میشود و سپس از من سوال میشود که آیا IPSEC فعال شود یا خیر که من y را وارد میکنم تا فعال شود
- سپس از من سوال میشود که ریست تایمر IPSEC چه باشد که من 2 دقیقه قرار میدهم. شما میتوانید مقدار دیگری قرار دهید

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/d34e615d-3e68-48d6-b27c-910d985dd1dc" alt="Image" />
</p>

- سپس از من سوال میشود که ایا میخواهم لوکال تانل من بر اساس بازه زمانی خاصی، ریست شود که من y را وارد میکنم و مقدار یک ساعت را وارد میکنم. شما میتوانید n بزنید که غیرفعال شود یا مقدار دیگری برای زمان انتخاب نمایید.(این عدد ها قابل تغییر است و فقط برای نمونه استفاده شده است)

---------------
 </details>
</div>
</details>
</div>  
<div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش ISATAP یک سرور ایران و دو کلاینت خارج</summary>

---------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور ایران**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/8d4afc22-0832-4472-8787-6f20578ed26b" alt="Image" />
</p>

- من 1 سرور ایران و 2 کلاینت خارج دارم.
- نخست ایپی 4 سرور ایران را وارد میکنم
- از من پرسیده میشود که mtu را به صورت manual وارد میکنید یا خیر. من n را وارد میکنم
- ایپی پرایوت شما نمایش داده میشود و سپس از من سوال میشود که چه تعداد کلاینت خارج دارم. من دو عدد کلاینت خارج دارم پس عدد 2 را وارد میکنم.
- ایپی 4 کلاینت اول خارج و پورت مورد نظر را وارد میکنم ( برای هر کلاینت باید پورت متفاوتی بدهید و ufw این پورت را به فایروال اضافه میکند)
- ایپی 4 کلاینت دوم خارج و پورت مورد نظر را وارد میکنم
- اگر از ufw استفاده میکنید بهتر است قبل از انجام کانفیگ، آن را disable کنید و سپس enable کنید یا ufw reload
- نخست از من سوال میشود که چند سرور ایران دارم. من دو سرور خارج دارم پس عدد 2 را وارد میکنم.
- سپس از من سوال میشود که ایا IPSEC فعال شود که من y را وارد میکنم و سپس secret key را azumi وارد میکنم ( شما میتوانید پیچیده تر بذارید)

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/84c50c16-e0f7-4af3-9df2-f19937ed2bad" alt="Image" />
</p>


- سپس از من میپرسد که ریست تایمر IPSEC بر چه اساس و unit ای باشد. من دقیقه را وارد میکنم و عدد 2 را وارد میکنم. مقدار شما میتواند متفاوت باشد
- سپس از من سوال میشود که ایا میخواهم لوکال من بر اساس زمانی خاص ریست شود که برای تست من گزینه y را وارد میکنم و به طور مثال هر ساعت میخواهم که این ریست انجام شود
- دقت نمایید شما میتوانید گزینه n را وارد کنید و ریست تایمر لوکال را فعال نکنید.
- اگر خطای بافر سایز گرفتید لطفا اطمینان حاصل فرمایید که روش های قبلی که در تضاد است ، پاک کرده باشید.
- از طریق گزینه Status میتوانید از فعال بودن روش و ایپی های کلاینت و سایر موارد آگاه شوید.

---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **کلاینت خارج اول**

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/1ee7b7a3-2927-40eb-a57b-26bda378c1cb" alt="Image" />
</p>

- کلاینت خارج اول را کانفیگ میکنم.
- ایپی 4 کلاینت اول خارج را وارد میکنم
- سپس ایپی 4 سرور ایران را وارد میکنم و به صورت اتومات prefix سرور ایران در کلاینت اضافه میشود.
- پورتی که برای کلاینت خارج اول را وارد کرده بودم را اینجا وارد میکنم که 5050 بود
- از من سوال میشود که mtu را manual وارد کنم که n را میزنم تا اتومات انتخاب شود.
- ایپی پرایوت این کلاینت نمایش داده میشود و سپس از من سوال میشود که آیا IPSEC فعال شود یا خیر که من y را وارد میکنم تا فعال شود
- سپس از من سوال میشود که ریست تایمر IPSEC چه باشد که من 2 دقیقه قرار میدهم. شما میتوانید مقدار دیگری قرار دهید

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/99125f0b-470f-4dad-b5e2-bf1bc5a03828" alt="Image" />
</p>

- سپس از من سوال میشود که ایا میخواهم لوکال تانل من بر اساس بازه زمانی خاصی، ریست شود که من y را وارد میکنم و مقدار یک ساعت را وارد میکنم. شما میتوانید n بزنید که غیرفعال شود یا مقدار دیگری برای زمان انتخاب نمایید.(این عدد ها قابل تغییر است و فقط برای نمونه استفاده شده است)

---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **کلاینت خارج دوم**

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/53162afd-5a8d-4f6c-bc3a-4f592c8f6d7b" alt="Image" />
</p>

- کلاینت خارج دوم را کانفیگ میکنم.
- ایپی 4 کلاینت دوم خارج را وارد میکنم
- سپس ایپی 4 سرور ایران را وارد میکنم و به صورت اتومات prefix سرور ایران در کلاینت دوم اضافه میشود.
- پورتی که برای کلانت خارج دوم را وارد کرده بودم را اینجا وارد میکنم که 5051 بود
- از من سوال میشود که mtu را manual وارد کنم که n را میزنم تا اتومات انتخاب شود.
- ایپی پرایوت این کلاینت نمایش داده میشود و سپس از من سوال میشود که آیا IPSEC فعال شود یا خیر که من y را وارد میکنم تا فعال شود
- سپس از من سوال میشود که ریست تایمر IPSEC چه باشد که من 2 دقیقه قرار میدهم. شما میتوانید مقدار دیگری قرار دهید

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/d34e615d-3e68-48d6-b27c-910d985dd1dc" alt="Image" />
</p>

- سپس از من سوال میشود که ایا میخواهم لوکال تانل من بر اساس بازه زمانی خاصی، ریست شود که من y را وارد میکنم و مقدار یک ساعت را وارد میکنم. شما میتوانید n بزنید که غیرفعال شود یا مقدار دیگری برای زمان انتخاب نمایید.(این عدد ها قابل تغییر است و فقط برای نمونه استفاده شده است)

---------------
 </details>
</div>

 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش IP6IP6 IPSEC  | ایپی پرایوت 6</summary>
    
  
------------------------------------ 


![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/902a2efa-f48f-4048-bc2a-5be12143bef3) **سرور خارج و ایران** 



- **من دو سرور خارج دارم و یک سرور ایران و میخواهم بوسیله IP6IP6 و IPSEC تانل را برقرار کنم**
- وارد گزینه IP6IP6 + IPSEc میشوم و گزینه 5 خارج و یک ایران را انتخاب میکنم.
- سرور اول و دوم خارج را کانفیگ میکنم و عدد MTU مناسب را وارد میکنم
- در سرور ایران تعداد سرور خارج را 2 انتخاب میکنم و هر دو سرور را کانفیگ میکنم و عدد MTU مناسب را وارد میکنم
- دقت کنید که اسکریپت های دیگر باعث از بین رفتن کامند های من در کرون نشود که باعث از بین رفتن تانل پس از ریبوت و از کار افتادن ریست تایمر IPSEC میشود.
- ریست تایمر IPSEC بهتر است بین 2 تا 5 دقیقه باشد و میتوانید از طریق گزینه ویرایش در خود IP6IP6 + IPSEC ، این مقدار را وارد نمایید
- دقت نمایید از ایپی اضافه (ایپی پرایوت دوم) برای پورت فوروارد یا تانل استفاده ننمایید و تنها از ایپی نخستین خود در تانل یا پورت فوروارد استفاده نمایید( بعدا قابلیت ایپی اضافه برای ipsec حذف خواهد شد){در اپدیت جدید ، ایپی اضافه برای Ipsec حذف شد}
- با این دستور سرویس موردنظر systemctl restart strong-azumi1 ریست میشود.

------------------

  </details>
</div>  

 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش IP6IP6 بین 3 سرور خارج و 1 سرور ایران</summary>

---------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور خارج اول**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/427104fe-0e38-4f87-a15c-387fbf10d3c1" alt="Image" />
</p>

- خب من 2 سرور خارج و 1 سرور ایران دارم و میخواهم از طریق IP6IP6 این تانل را برقرار کنم
- نخست سرور خارج اول را کانفیگ میکنم
- ایپی 4 سرور اول خارج را وارد میکنم.
- ایپی 4 سرور ایران را وارد میکنم ( ایپی سرور ایران برای تمامی سرور های خارج یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- سپس دوباره از من میخواهد که IP6IP6 MTU را تنظیم کنم
- سپس ایپی های GENERATE شده را میتوانید مشاهده کنید.
---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور خارج دوم**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/4db46ac0-fac0-4086-8e48-9fad2e7e7e0f" alt="Image" />
</p>

- سرور خارج دوم را کانفیگ میکنم
- ایپی 4 سرور دوم خارج را وارد میکنم.
- ایپی 4 سرور ایران را وارد میکنم ( ایپی سرور ایران برای تمامی سرور های خارج یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- سپس دوباره از من میخواهد که IP6IP6 MTU را تنظیم کنم
- سپس ایپی های GENERATE شده را میتوانید مشاهده کنید.
---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور ایران**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/229a0767-705a-4782-b55a-f628f7d34dd5" alt="Image" />
</p>

- سرور ایران را کانفیگ میکنم
- نخست از من میپرسد که چه تعداد سرور خارج دارم. من 2 عدد سرور خارج دارم
- کانفیگ سرور اول آغاز میشود و ایپی 4 سرور اول خارج را وارد میکنم.
- ایپی 4 سرور ایران را وارد میکنم ( ایپی سرور ایران برای تمامی سرور های خارج یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- سپس دوباره از من میخواهد که IP6IP6 MTU را تنظیم کنم
- سپس ایپی های GENERATE شده برای سرور اول را میتوانید مشاهده کنید.
<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/0bd168a7-6b2b-4561-84b2-0bd84ee5c283" alt="Image" />
</p>

- کانفیگ سرور دوم آغاز میشود و ایپی 4 سرور دوم خارج را وارد میکنم.
- ایپی 4 سرور ایران را وارد میکنم ( ایپی سرور ایران برای تمامی سرور های خارج یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- سپس دوباره از من میخواهد که IP6IP6 MTU را تنظیم کنم
- سپس ایپی های GENERATE شده برای سرور دوم را میتوانید مشاهده کنید.
---------------

 </details>
</div>
<div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش IP6IP6 بین 3 سرور ایران و 1 سرور خارج</summary>

---------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور خارج**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/b1d391f9-06da-4fcd-81f7-7390e006e0d3" alt="Image" />
</p>

- خب من 2 سرور ایران و 1 سرور خارج دارم و میخواهم از طریق IP6IP6 این تانل را برقرار کنم
- نخست سرور خارج را کانفیگ میکنم
- از من سوال میشود چند سرور ایران دارم ، من 2 عدد سرور ایران دارم پس عدد 2 را وارد میکنم
- ایپی 4 سرور اول ایران را وارد میکنم.
- ایپی 4 سرور خارج را وارد میکنم ( ایپی سرور خارج برای تمامی سرور های ایران یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- سپس دوباره از من میخواهد که IP6IP6 MTU را تنظیم کنم
- سپس ایپی های GENERATE شده برای سرور اول را میتوانید مشاهده کنید.

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/5eb12947-727f-4cfd-853f-cf628a49f7dc" alt="Image" />
</p>

- ادامه کانفیگ را انجام میدم
- ایپی 4 سرور دوم ایران را وارد میکنم.
- ایپی 4 سرور خارج را وارد میکنم ( ایپی سرور خارج برای تمامی سرور های ایران یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- سپس دوباره از من میخواهد که IP6IP6 MTU را تنظیم کنم
- سپس ایپی های GENERATE شده برای سرور دوم را میتوانید مشاهده کنید.
---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور ایران اول**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/72ea230e-0a1f-4b1c-9978-0de598f8ae67" alt="Image" />
</p>

- سرور ایران اول را کانفیگ میکنم
- ایپی 4 سرور اول ایران را وارد میکنم.
- ایپی 4 سرور خارج را وارد میکنم (ایپی سرور خارج برای تمامی سرور های ایران یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- در سرور ایران default route را تغییر میدهم پس گزینه yes رو میزنم . شما میتوانید گزینه No را بزنید.
- سپس دوباره از من میخواهد که IP6IP6 MTU را تنظیم کنم
- سپس ایپی های GENERATE شده را میتوانید مشاهده کنید.
---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور ایران دوم**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/cafd52b7-6802-4359-bd61-731ed1a0a409" alt="Image" />
</p>

- سرور ایران دوم را کانفیگ میکنم
- ایپی 4 سرور دوم ایران را وارد میکنم.
- ایپی 4 سرور خارج را وارد میکنم (ایپی سرور خارج برای تمامی سرور های ایران یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- در سرور ایران default route را تغییر میدهم پس گزینه yes رو میزنم . شما میتوانید گزینه No را بزنید.
- سپس دوباره از من میخواهد که IP6IP6 MTU را تنظیم کنم
- سپس ایپی های GENERATE شده را میتوانید مشاهده کنید.
---------------

 </details>
</div>
<div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش GRE6 بین 3 سرور خارج و 1 سرور ایران</summary>

---------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور خارج اول**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/85e4985a-161d-43b3-9314-afed32e49e84" alt="Image" />
</p>

- خب من 2 سرور خارج و 1 سرور ایران دارم و میخواهم از طریق GRE6 این تانل را برقرار کنم
- نخست سرور خارج اول را کانفیگ میکنم
- ایپی 4 سرور اول خارج را وارد میکنم.
- ایپی 4 سرور ایران را وارد میکنم ( ایپی سرور ایران برای تمامی سرور های خارج یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- سپس دوباره از من میخواهد که  GRE6 MTU را تنظیم کنم
- سپس ایپی های GENERATE شده را میتوانید مشاهده کنید.
---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور خارج دوم**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/d0b25c30-4fcb-49ae-aaec-328983b6c828" alt="Image" />
</p>

- سرور خارج دوم را کانفیگ میکنم
- ایپی 4 سرور دوم خارج را وارد میکنم.
- ایپی 4 سرور ایران را وارد میکنم ( ایپی سرور ایران برای تمامی سرور های خارج یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- سپس دوباره از من میخواهد که GRE6 MTU را تنظیم کنم
- سپس ایپی های GENERATE شده را میتوانید مشاهده کنید.
---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور ایران**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/4e265f17-22fc-4520-bdbe-ec783632bf55" alt="Image" />
</p>

- سرور ایران را کانفیگ میکنم
- نخست از من میپرسد که چه تعداد سرور خارج دارم. من 2 عدد سرور خارج دارم
- کانفیگ سرور اول آغاز میشود و ایپی 4 سرور اول خارج را وارد میکنم.
- ایپی 4 سرور ایران را وارد میکنم ( ایپی سرور ایران برای تمامی سرور های خارج یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- سپس دوباره از من میخواهد که GRE6 MTU را تنظیم کنم
- سپس ایپی های GENERATE شده برای سرور اول را میتوانید مشاهده کنید.

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/d8165985-da76-4659-9a81-2c9b009902e2" alt="Image" />
</p>

- کانفیگ سرور دوم آغاز میشود و ایپی 4 سرور دوم خارج را وارد میکنم.
- ایپی 4 سرور ایران را وارد میکنم ( ایپی سرور ایران برای تمامی سرور های خارج یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- سپس دوباره از من میخواهد که GRE6 MTU را تنظیم کنم
- سپس ایپی های GENERATE شده برای سرور دوم را میتوانید مشاهده کنید.
---------------

 </details>
</div>
<div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش GRE6 بین 3 سرور ایران و 1 سرور خارج</summary>

---------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور خارج**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/851dd5d3-624a-4993-af2d-5e4eea861e08" alt="Image" />
</p>

- خب من 2 سرور ایران و 1 سرور خارج دارم و میخواهم از طریق GRE6 این تانل را برقرار کنم
- نخست سرور خارج را کانفیگ میکنم
- از من سوال میشود چند سرور ایران دارم ، من 2 عدد سرور ایران دارم پس عدد 2 را وارد میکنم
- ایپی 4 سرور اول ایران را وارد میکنم.
- ایپی 4 سرور خارج را وارد میکنم ( ایپی سرور خارج برای تمامی سرور های ایران یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- سپس دوباره از من میخواهد که GRE6 MTU را تنظیم کنم
- سپس ایپی های GENERATE شده برای سرور اول را میتوانید مشاهده کنید.

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/99b82ecd-b02d-4d2a-94d4-d69143cce8f8" alt="Image" />
</p>

- ادامه کانفیگ را انجام میدم
- ایپی 4 سرور دوم ایران را وارد میکنم.
- ایپی 4 سرور خارج را وارد میکنم ( ایپی سرور خارج برای تمامی سرور های ایران یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- سپس دوباره از من میخواهد که GRE6 MTU را تنظیم کنم
- سپس ایپی های GENERATE شده برای سرور دوم را میتوانید مشاهده کنید.
---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور ایران اول**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/563653c9-f1b3-4128-9bd4-5aa4bccf50ab" alt="Image" />
</p>

- سرور ایران اول را کانفیگ میکنم
- ایپی 4 سرور اول ایران را وارد میکنم.
- ایپی 4 سرور خارج را وارد میکنم (ایپی سرور خارج برای تمامی سرور های ایران یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- در سرور ایران default route را تغییر میدهم پس گزینه yes رو میزنم . شما میتوانید گزینه No را بزنید.
- سپس دوباره از من میخواهد که GRE6 MTU را تنظیم کنم
- سپس ایپی های GENERATE شده را میتوانید مشاهده کنید.
---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور ایران دوم**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/cafd52b7-6802-4359-bd61-731ed1a0a409" alt="Image" />
</p>

- سرور ایران دوم را کانفیگ میکنم
- ایپی 4 سرور دوم ایران را وارد میکنم.
- ایپی 4 سرور خارج را وارد میکنم (ایپی سرور خارج برای تمامی سرور های ایران یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- در سرور ایران default route را تغییر میدهم پس گزینه yes رو میزنم . شما میتوانید گزینه No را بزنید.
- سپس دوباره از من میخواهد که GRE6 MTU را تنظیم کنم
- سپس ایپی های GENERATE شده را میتوانید مشاهده کنید.

 ---------------------------------------
 
 </details>
</div>
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش 6TO4 بین 5 سرور خارج و 1 سرور ایران</summary>

---------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور خارج اول**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/8ad6ffa8-b9f4-449c-9cbe-c6b8442a5306" alt="Image" />
</p>

- خب من 2 سرور خارج و 1 سرور ایران دارم و میخواهم از طریق 6TO4 این تانل را برقرار کنم
- نخست سرور خارج اول را کانفیگ میکنم
- ایپی 4 سرور اول خارج را وارد میکنم.
- ایپی 4 سرور ایران را وارد میکنم ( ایپی سرور ایران برای تمامی سرور های خارج یکسان است)
- تعداد ایپی اضافه را 1 انتخاب میکنم
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- سپس ایپی های GENERATE شده را میتوانید مشاهده کنید.
---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور خارج دوم**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/0e463162-0184-4f2d-96d6-c0fd4cf0c849" alt="Image" />
</p>

- سرور خارج دوم را کانفیگ میکنم
- ایپی 4 سرور دوم خارج را وارد میکنم.
- تعداد ایپی اضافه را 1 انتخاب میکنم
- ایپی 4 سرور ایران را وارد میکنم ( ایپی سرور ایران برای تمامی سرور های خارج یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- سپس ایپی های GENERATE شده را میتوانید مشاهده کنید.
---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور ایران**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/a17229b0-a725-45e4-b2ef-387528d8bc56" alt="Image" />
</p>

- سرور ایران را کانفیگ میکنم
- نخست از من میپرسد که چه تعداد سرور خارج دارم. من 2 عدد سرور خارج دارم
- کانفیگ سرور اول آغاز میشود و ایپی 4 سرور اول خارج را وارد میکنم.
- ایپی 4 سرور ایران را وارد میکنم ( ایپی سرور ایران برای تمامی سرور های خارج یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- سپس ایپی های GENERATE شده برای سرور اول را میتوانید مشاهده کنید.

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/08de50f2-4cef-4321-949d-072fc31c85fd" alt="Image" />
</p>

- کانفیگ سرور دوم آغاز میشود و ایپی 4 سرور دوم خارج را وارد میکنم.
- ایپی 4 سرور ایران را وارد میکنم ( ایپی سرور ایران برای تمامی سرور های خارج یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- سپس ایپی های GENERATE شده برای سرور دوم را میتوانید مشاهده کنید.
---------------

 </details>
</div>
<div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش 6TO4 بین 5 سرور ایران و 1 سرور خارج</summary>

---------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور خارج**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/8b1b1310-a218-47a1-ae94-31c90d679d66" alt="Image" />
</p>

- خب من 2 سرور ایران و 1 سرور خارج دارم و میخواهم از طریق 6TO4 این تانل را برقرار کنم
- نخست سرور خارج را کانفیگ میکنم
- از من سوال میشود چند سرور ایران دارم ، من 2 عدد سرور ایران دارم پس عدد 2 را وارد میکنم
- ایپی 4 سرور اول ایران را وارد میکنم.
- ایپی 4 سرور خارج را وارد میکنم ( ایپی سرور خارج برای تمامی سرور های ایران یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- سپس ایپی های GENERATE شده برای سرور اول را میتوانید مشاهده کنید.

<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/4fff1f7d-ec19-4c8c-a0e5-19eff01aeffa" alt="Image" />
</p>

- ادامه کانفیگ را انجام میدم
- ایپی 4 سرور دوم ایران را وارد میکنم.
- ایپی 4 سرور خارج را وارد میکنم ( ایپی سرور خارج برای تمامی سرور های ایران یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- سپس ایپی های GENERATE شده برای سرور دوم را میتوانید مشاهده کنید.
---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور ایران اول**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/d771b747-6046-4a1e-a1b1-f85e5a5df925" alt="Image" />
</p>

- سرور ایران اول را کانفیگ میکنم
- ایپی 4 سرور اول ایران را وارد میکنم.
- ایپی 4 سرور خارج را وارد میکنم (ایپی سرور خارج برای تمامی سرور های ایران یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- در سرور ایران default route را تغییر میدهم پس گزینه yes رو میزنم . شما میتوانید گزینه No را بزنید.
- سپس ایپی های GENERATE شده را میتوانید مشاهده کنید.
---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور ایران دوم**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/21a4e1bd-878a-4297-af6a-cac38488eabc" alt="Image" />
</p>

- سرور ایران دوم را کانفیگ میکنم
- ایپی 4 سرور دوم ایران را وارد میکنم.
- ایپی 4 سرور خارج را وارد میکنم (ایپی سرور خارج برای تمامی سرور های ایران یکسان است)
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- تعداد ایپی اضافه را 1 انتخاب میکنم
- در سرور ایران default route را تغییر میدهم پس گزینه yes رو میزنم . شما میتوانید گزینه No را بزنید.
- سپس ایپی های GENERATE شده را میتوانید مشاهده کنید.
---------------

 </details>
</div>
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>روش ANYCAST پنج سرور خارج و ایران</summary>

---------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور ایران اول**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/92314ffc-71b6-4317-9a4c-3580414935e9" alt="Image" />
</p>

- خب من 2 سرور ایران و 1 سرور خارج دارم و میخواهم از طریق این روش، این تانل را برقرار کنم
- شما میتوانید 3 سرور ایران و 3 سرور خارج را کانفیگ کنید. در اینجا برای اموزش صرفا از 2 سرور ایران و یک ایپی خارج استفاده میکنم. لطفا آموزش را با دقت بخوانید.
- نخست سرور ایران اول را کانفیگ میکنم
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- مسیر دیفالت روت را در سرور ایران تغییر میدهم پس گزینه YES را انتخاب میکنم.
- من 3 سرور دارم. در حال حاضر داخل سرور اول ایران هستم.از من سوال میشود که چه تعداد سرور دارم ( این سوال برای سرویس پینگ است). پس باید دو سرویس پینگ برای دو سرور دیگر درست کنم. پس عدد 2 را وارد میکنم که 2 عدد سرویس پینگ ایجاد شود
- ایپی 4 ادرس سرور های دیگر را وارد میکنم. پس ایپی ادرس سرور ایران دوم و ایپی ادرس سرور خارج را وارد میکنم. همین کار باید در سرور های دیگر هم انجام شود وگرنه ممکن است به مشکل بخورید.
- با دستور ip a میتوانید ایپی های generate شده را ببینید.
---------------
![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور ایران دوم**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/748ab862-a94c-4b63-ac29-b2f81a70df8c" alt="Image" />
</p>


- سرور ایران دوم را کانفیگ میکنم
- ایپی 4 سرور ایران دوم را وارد میکنم.
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- مسیر دیفالت روت را در سرور ایران تغییر میدهم پس گزینه YES را انتخاب میکنم.
- من 3 سرور دارم. در حال حاضر داخل سرور دوم ایران هستم.از من سوال میشود که چه تعداد سرور دارم ( این سوال برای سرویس پینگ است). پس باید دو سرویس پینگ برای دو سرور دیگر درست کنم. پس عدد 2 را وارد میکنم که 2 عدد سرویس پینگ ایجاد شود
- ایپی 4 ادرس سرور های دیگر را وارد میکنم. پس ایپی ادرس سرور ایران اول و ایپی ادرس سرور خارج را وارد میکنم. همین کار باید در سرور های دیگر هم انجام شود وگرنه ممکن است به مشکل بخورید.
- با دستور ip a میتوانید ایپی های generate شده را ببینید.
---------------

![green-dot-clipart-3](https://github.com/Azumi67/6TO4-PrivateIP/assets/119934376/c14c77ec-dc4e-4c8a-bdc2-4dc4e42a1815) **سرور خارج**


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/325512ab-351b-478d-b446-4aed2ee702fb" alt="Image" />
</p>


- سرور خارج را کانفیگ میکنم
- ایپی 4 سرور خارج را وارد میکنم.
- سپس میتوانم گزینه Y را بزنم و MTU را به صورت دستی وارد نمایم یا گزینه N را بزنم و به صورت AUTO این کار انجام شود. بعدا میتوانید MTU را در منو اسکریپت ویرایش نمایید
- من 3 سرور دارم. در حال حاضر داخل سرور خارج هستم.از من سوال میشود که چه تعداد سرور دارم ( این سوال برای سرویس پینگ است). پس باید دو سرویس پینگ برای دو سرور دیگر درست کنم. پس عدد 2 را وارد میکنم که 2 عدد سرویس پینگ ایجاد شود
- ایپی 4 ادرس سرور های دیگر را وارد میکنم. پس ایپی ادرس سرور ایران اول و ایپی ادرس سرور ایران دوم را وارد میکنم. همین کار باید در سرور های دیگر هم انجام شود وگرنه ممکن است به مشکل بخورید.
- با دستور ip a میتوانید ایپی های generate شده را ببینید.

---------------

 </details>
</div>
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>نحوه ویرایش mtu</summary>

---------------



<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/13c54935-60d5-42cd-801a-ba5092a44a45" alt="Image" />
</p>

- برای نمونه من میخواهم mtu دو تانلی 6to4 ای که در سرور خارج ساختم را ویرایش کنم. نخست وارد قسمت ویرایش Mtu میشوم و کانفیگ 5 سرور ایران و 1 سرور خارج را انتخاب میکنم
- سپس سرور خارج را انتخاب میکنم. حالا در این منو میتوانم 5 تانل 6to4 که درست کرده ام را ویرایش کنم . من دو سرور ایران داشتم پس 2 تانل در سرور خارج درست شده است
- میتوانم به صورت جداگانه mtu این تانل ها را ویرایش کنم یا به صورت دست جمعی
- به طور مثال mtu تانل سرور اول و دوم را میتوانم به صورت جداگانه ویرایش کنم . اما در این آموزش من به صورت دست جمعی را نشان میدهم. بقیه را خودتان ازمون و خطا کنید.
- پس گزینه all of them را انتخاب میکنم و تعداد سرور ایران هم 2 وارد میکنم که در سرور خارج دو تانل 6to4 ایجاد شده را ویرایش کنم
- برای سرور اول mtu انتخابی خود را قرار میدم و سپس همینکار را برای سرور دوم انجام میدم
- به این صورت شما میتوانید به سادگی mtu های تانل ها و سرور های خود را ویرایش کنید.
- دقت نمایید که در مسیر مربوطه بروید و به اشتباه تانل دیگر را ویرایش نکنید
- دقت نمایید که سرور های خود را بدانید که کدام به کدام است و اشتباه ویرایش نکنید.
---------------

 </details>
</div>


 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/Azumi67/Rathole_reverseTunnel/assets/119934376/fcbbdc62-2de5-48aa-bbdd-e323e96a62b5" alt="Image"> </strong>نحوه پاک کردن</summary>

---------------


<p align="right">
  <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/56b75075-4012-4c2e-928c-3fad2d9fc984" alt="Image" />
</p>

- برای نمونه من میخواهم سرویس و ایپی های ایجاد شده برای gre6 را پاک کنم. تانل من 3 سرور ایران و یک سرور خارج میباشد و میخواهم در سرور خارج عملیات پاک کردن را انجام بدهم.
- نخست وارد گزینه gre6 میشوم و گزینه 3 سرور ایران و 1 سرور خارج را انتخاب میکنم.
- گزینه 4 سرور خارج را انتخاب میکنم.
- از من سوال میشود که چه تعداد سرور ایران دارم. من دو عدد داشتم پس عدد 2 را وارد میکنم
- سپس تمامی سرویس ها و ایپی ها پاک میشود
- دقت نمایید که در مسیر درست هستید وگرنه عملیات پاک کردن به درستی انجام نمیشود.
 </details>
</div>

---------------
**اسکرین شات**
<details>
  <summary align="right">Click to reveal image</summary>
  
  <p align="right">
    <img src="https://github.com/Azumi67/6TO4-GRE-IPIP-SIT/assets/119934376/40e01e48-64d9-4160-a6e9-545f4bde957d" alt="menu screen" />
  </p>
</details>


------------------------------------------
![scri](https://github.com/Azumi67/FRP-V2ray-Loadbalance/assets/119934376/cbfb72ac-eff1-46df-b5e5-a3930a4a6651)
**اسکریپت های کارآمد :**
- برای بهبود عملکرد سرور میتوانید از optimizer استفاده نمایید یا bbr ساده نصب کنید

Kalilovers Script [for ipsec]
```
python3 <(curl -Ls https://raw.githubusercontent.com/kalilovers/LightKnightBBR/main/bbr.py --ipv4)
```
 Opiran Script
```
apt install curl -y && bash <(curl -s https://raw.githubusercontent.com/opiran-club/VPS-Optimizer/main/optimizer.sh --ipv4)
```

Hawshemi script

```
wget "https://raw.githubusercontent.com/hawshemi/Linux-Optimizer/main/linux-optimizer.sh" -O linux-optimizer.sh && chmod +x linux-optimizer.sh && bash linux-optimizer.sh
```

-----------------------------------------------------
![R (a2)](https://github.com/Azumi67/PrivateIP-Tunnel/assets/119934376/716fd45e-635c-4796-b8cf-856024e5b2b2)
**اسکریپت من**
----------------

- نصب یش نیاز ها
```
apt install python3 -y && sudo apt install python3-pip &&  pip install colorama && pip install netifaces && apt install curl -y
pip3 install colorama
sudo apt-get install python-pip -y  &&  apt-get install python3 -y && alias python=python3 && python -m pip install colorama && python -m pip install netifaces
```
- نسخه پایین برای سرور های دارای رم کمتر میباشد
```
bash -c "$(curl -fsSL https://raw.githubusercontent.com/Digitalvps-Ir/6TO4-GRE-IPIP-SIT/main/lightweight.sh)"
```
- نسخه پایین برای سرور های دارای رم کمتر و externally managed
```
bash -c "$(curl -fsSL https://raw.githubusercontent.com/Digitalvps-Ir/6TO4-GRE-IPIP-SIT/main/managed4.sh)"
```

------------------
- برای ubuntu24 و حتی سایر سیستم عامل ها میتوانید از این دستور استفاده نمایید ( پیش نیاز ها نصب شده باشد)- این نسخه برای سرور های با رم بالا است
```
bash -c "$(curl -fsSL https://raw.githubusercontent.com/Digitalvps-Ir/6TO4-GRE-IPIP-SIT/main/ubuntu24.sh)"
```
- برای ubuntu24 و سیستم عامل های دیگر با خطای externally managed - این نسخه برای سرور های با رم بالا است
```
bash -c "$(curl -fsSL https://raw.githubusercontent.com/Digitalvps-Ir/6TO4-GRE-IPIP-SIT/main/managed3.sh)"
```
----------------
- نسخه های پایین ممکن است برای همه قابل اجرا نباشد و برای سرور های با رم بالا است
```
apt install python3 -y && sudo apt install python3-pip &&  pip install colorama && pip install netifaces && apt install curl -y && python3 <(curl -Ls https://raw.githubusercontent.com/Digitalvps-Ir/6TO4-GRE-IPIP-SIT/main/ipipv2.py --ipv4)
```


- اگر با دستور بالا نتوانستید اسکریپت را اجرا کنید، نخست دستور زیر را اجرا نمایید و سپس دستور اول را دوباره اجرا کنید.
- اگر باز هم colorama نصب نشد، دستور روبرو هم اجرا کنید .  pip3 install colorama

```
sudo apt-get install python-pip -y  &&  apt-get install python3 -y && alias python=python3 && python -m pip install colorama && python -m pip install netifaces
```
--------------------------------------
 <div dir="rtl">&bull;  دستور زیر برای کسانی هست که پیش نیاز ها را در سرور، نصب شده دارند</div>
 
```
python3 <(curl -Ls https://raw.githubusercontent.com/Digitalvps-Ir/6TO4-GRE-IPIP-SIT/main/ipipv2.py --ipv4)
```
--------------------------------------
 <div dir="rtl">&bull; اگر سرور شما خطای externally-managed-environment داد از دستور زیر اقدام به اجرای اسکریپت نمایید.</div>
 
```
bash -c "$(curl -fsSL https://raw.githubusercontent.com/Digitalvps-Ir/6TO4-GRE-IPIP-SIT/main/managed2.sh)"
```
---------------------------------------------



