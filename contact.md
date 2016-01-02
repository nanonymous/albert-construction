---
layout: page
title: Контакты
permalink: /contact/
order: 3
---

<p class="contacts">
    <i class="material-icons">person</i> {{ site.contact_title }}<br/>
	<!-- <i class="material-icons" style="visibility: hidden">person</i> <span style="font-style:italic">главный специалист</span><br/> -->

	<i class="material-icons">phone</i> {{ site.phone }}<br/>
    <i class="material-icons">mail</i> <a href="mailto:{{ site.email }}">{{ site.email }}</a><br/>

    <br/>

	<i class="material-icons">place</i> Санкт-Петербург, Аптекарский переулок, 4<br/>
	офис 302<br/>
	<i class="material-icons">access_time</i> будни, c 9 до 18<br/>
</p>

<div id="contact-map"></div>

<script type="text/javascript">
	function yandex_map(ymaps)
	{
	    var map = new ymaps.Map("contact-map",
	    {
            center: [59.943, 30.328181], 
            zoom: 16,
    		controls: ['zoomControl', 'typeSelector', 'fullscreenControl']
        })

	    if (map)
	    {
	    	var placemark = new ymaps.Placemark([59.942952, 30.329104],
	    	{
	            // balloonContent: '<b>Albert Construction</b><br/>Аптекарский переулок, 4<br/>офис 302'
			    balloonContentBody:
			    [
		            '<address style="font-style: normal">',
		            '<strong>Albert Construction</strong>',
		            '<br/>',
		            'Адрес: 119021, Санкт-Петербург, Аптекарский переулок, 4',
		            '<br/>',
		            'Подробнее: <a href="https://company.yandex.ru/">https://company.yandex.ru</a>',
		            '</address>'
		        ].join('')

	        },
	        {
	            preset: 'islands#redDotIcon',
	            // iconColor: '#0095b6'
	        })

	        // placemark.openBalloon()

	        map.geoObjects.add(placemark)
	    }
	}
</script>

<script src="https://api-maps.yandex.ru/2.1/?onload=yandex_map&lang=ru_RU" type="text/javascript"> </script>