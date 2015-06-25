# lazyload
# description: lazy load image and data

/**
 * global variable
 */
var $small_version = false, $is_webp = false;

/**
 * invoke method
 */
$('img.lazy').lazyload({
    data_attribute: $small_version ? 'so' : 'bo', //small and big version switch.
		container: $(window),
	  callback: foot_lazy
});

/**
 * touch container for execute foot lazy
 */
foot_lazy ()
{
    /*Begin TODO:icon group*/
    if($is_webp)
    {
        $('#b-ico').html('<a href=""><img class="lazy" src="/img/unit/blank.gif" data-bo="/img/5.0/big-picture.webp" data-so="/img/5.0/small-picture.webp"></a>');
    }else{
        $('#b-ico').html('<a href=""><img class="lazy" src="/img/unit/blank.gif" data-bo="/img/5.0/big-picture.jpg" data-so="/img/5.0/small-picture.jpg"></a>');
    }
    /*End TODO:icon group*/

}
