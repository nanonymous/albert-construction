---
layout: page
title: Связаться с нами
permalink: /contact/
order: 3
---

<p>
    {{ site.contact_title }}<br/>
	главный специалист<br/>

    {{ site.phone }}<br/>
    <a href="mailto:{{ site.email }}">{{ site.email }}</a><br/>

    <br/>

	г. Санкт-Петербург<br/>
	Аптекарский переулок, 4<br/>
	офис 302<br/>
	будни, c 9 до 18<br/>
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