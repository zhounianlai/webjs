# webjs
页面常用javascript特效

<script>
function pop(id,idbg,popW,popH){
    var winW = window.innerWidth;
    var winH = window.innerHeight;
    var pop = document.getElementById(id);
    var bg = document.getElementById(idbg);
    var bW = (winW-popW)/2+"px";
    var bH = (winH-popH)/2+"px";
    pop.setAttribute("style", "left:" + bW + ";top:" + bH +";display:block");
    bg.style.display="block";
}

function cloose(id,idbg){
    var pop = document.getElementById(id);
    var bg = document.getElementById(idbg);
    pop.style.display="none";
    bg.style.display="none";
}

setTimeout("pop('pop','bg',650,619)",3000);

function popss(id,popW,popH){
    var winW = window.innerWidth;
    var winH = window.innerHeight;
    var pop = document.getElementById(id);
    var bW = (winW-popW)/2+"px";
    var bH = (winH-popH)/2+"px";
    pop.style.left=bW;
    pop.style.top=bH;
}

window.onresize = function(){
    popss('pop',650,619)
}
</script>
