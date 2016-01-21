# SVG-getTransformToElement-FIX
This is a drop-in replacement for the getTransformToElement removed from SVG2 
(https://lists.w3.org/Archives/Public/www-svg/2015Jun/0044.html)


Copy this code and paste it in your project

```
if( ! SVGElement.prototype.getTransformToElement)
{
	SVGElement.prototype.getTransformToElement = function( _element )
	{
		return _element.getCTM().inverse().multiply(  this.getCTM()  );
	};
}

```

this is a piece of code of janvas (SVG editor)

[janvas.com](http://www.janvas.com)
