<style>
 .vcenter { 
  display: inline-block;
  vertical-align: middle;
  float: none;
}
</style>

<div class="panel panel-primary">
<div class="panel-heading">
<strong>Institutions</strong>
</div>
<ul class="list-group">
{% for supporter in site.data.supporters %}
<li class="list-group-item">
  <div class="row">
  <div class="col-xs-7 col-md-9 vcenter"><a href="{{ supporter.link }}"><img style="max-height:100px;" class="img-responsive center-block" src="{{ supporter.logo }}" alt="{{supporter.name}}"></a></div><div class="col-xs-3 col-md-3 text-center text-muted vcenter">{% if supporter.tier %}{{supporter.tier | capitalize }} {% endif%}{{supporter.type}}</div>
  </div>
</li>
{% endfor %}
</ul>
</div>