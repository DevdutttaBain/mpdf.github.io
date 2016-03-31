---
layout: page
title: SetAlpha()
parent_title: mPDF functions
permalink: /reference/mpdf-functions/setalpha.html
modification_time: 2015-08-05T12:00:53+00:00
---

<p>(mPDF &gt;= 1.0)</p>
<p>SetAlpha – Set the opacity for Images</p>

# Description

<p class="manual_block">void <b>SetAlpha</b> ( float <span class="parameter">$alpha</span> [, integer <span class="parameter">$blend</span> ])</p>
<p>Set the opacity and blend mode for Images</p>

# Parameters

<p class="manual_param_dt"><span class="parameter">alpha</span></p>
<p class="manual_param_dd">This parameter specifies the opacity for any subsequent images written to the current document.</p>
<p class="manual_param_dd"><b>Values</b>

Float: 0 (transparent) to 1 (opaque)</p>
<p class="manual_param_dt"><span class="parameter">blend</span></p>
<p class="manual_param_dd">This parameter specifies the blend mode.</p>
<p class="manual_param_dd"><b>Values</b>

<span class="smallblock">STRING</span> - One of the following:

Normal

Multiply

Screen

Overlay

Darken

Lighten

ColorDodge

ColorBurn

HardLight

SoftLight

Difference

Exclusion

Hue

Saturation

Color

Luminosity

<span class="smallblock">DEFAULT</span>: Normal</p>

# Changelog

<table class="table"> <thead>
<tr> <th>Version</th><th>Description</th> </tr>
</thead> <tbody>
<tr>
<td>1.0</td>
<td>Function was added.</td>
</tr>
</tbody> </table>

# Examples

{% highlight php %}
Example #1
{% endhighlight %}

{% highlight php %}
<?php

<?php

include("../mpdf.php");

$mpdf=new mPDF();

$mpdf->SetAlpha(0.5); 

$mpdf->WriteHTML('<img src="clematis.jpg" />');

$mpdf->SetAlpha(1); 

// This produces the identical result as the last 3 lines

// $mpdf->WriteHTML('<img src="clematis.jpg" opacity="0.5" />');

$mpdf->Output();

exit;

?>
{% endhighlight %}

# See Also

<ul>
<li class="manual_boxlist"><a href="{{ "/reference/mpdf-functions/image.html" | prepend: site.baseurl }}">Image()</a> - Write an image to the current document</li>
</ul>
