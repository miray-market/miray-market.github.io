
<!DOCTYPE html>
<html>
<head>
  <meta http-equiv="content-type" content="text/html; charset=utf-8" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="author" content="Miray Market" />
  <meta name="description" content="Miray Market" />
  <meta name="keywords" content="miray, market, bakkal, kırtasiye, miray market, miray bakkal, miray kırtasiye, gaziantep market, gaziantep bakkal, gaziantep kırtasiye" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <title>Barak Framework Sayfalar</title>

  <link rel="shortcut icon" href="https://raw.githubusercontent.com/barak-framework/barak-framework.github.io/master/favicon.ico" />

  <!-- turkuazcss start -->
  <!-- source: https://github.com/turkuazcss/turkuazcss -->
  <link rel="stylesheet" type="text/css" href="https://barak-framework.github.io/assets/css/turkuaz.css" />
  <script src="https://barak-framework.github.io/assets/js/turkuaz.js"></script>
  <!-- turkuazcss end -->

  <!-- <link rel="stylesheet" type="text/css" href="https://barak-framework.github.io/assets/css/bootstrap.min.css" /> -->

  <!-- HTML5 shim and Respond.js IE8 support of HTML5 elements and media queries -->
  <!--[if lt IE 9]>

  <script src="https://barak-framework.github.io/assets/js/html5shiv.min.js"></script>
  <script src="https://barak-framework.github.io/assets/js/respond.min.js"></script>

  <![endif]-->

  <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
  <script src="https://code.jquery.com/jquery-latest.min.js"></script>
  <!-- <script src="https://barak-framework.github.io/assets/js/bootstrap.min.js"></script> -->

  <!-- Google Analytics start -->
  <script type="text/javascript">
  var _gaq = _gaq || [];
  _gaq.push(['_setAccount', 'UA-111463108-1']);

  _gaq.push(['_trackPageview']);
  (function() {
    var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
    ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
    var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
  })();
  </script>
  <!-- Google Analytics end -->

  <!-- Highlightjs start -->
  <!-- source: http://highlightjs.org -->
  <link rel="stylesheet" type="text/css" href="https://barak-framework.github.io/assets/css/highlight.pack.css" />
  <script src="https://barak-framework.github.io/assets/js/highlight.pack.js"></script>
  <script type="text/javascript">
  hljs.initHighlightingOnLoad();
  </script>
  <!-- Highlightjs end -->

  <!-- Animatecss start -->
  <!-- source: https://daneden.github.io/animate.css/ -->
  <link rel="stylesheet" type="text/css" href="https://barak-framework.github.io/assets/css/animate.min.css" />
  <!-- Animatecss end -->

  <!-- Github-markdown-css start -->
  <!-- source: https://github.com/sindresorhus/github-markdown-css -->
  <link rel="stylesheet" type="text/css" href="https://barak-framework.github.io/assets/css/github-markdown.css" />
  <style>
  .markdown-body {
    box-sizing: border-box;
    min-width: 200px;
    max-width: 980px;
    margin: 0 auto;
    padding: 45px;
  }

  @media (max-width: 767px) {
    .markdown-body {
      padding: 15px;
    }
  }
  </style>
  <!-- Github-markdown-css end -->

  <!-- Showdownjs start -->
  <!-- source: https://github.com/showdownjs/showdown -->
  <script src="https://barak-framework.github.io/assets/js/showdown.min.js"></script>
  <!-- Showdownjs end -->

  <!-- Moonmode start -->
  <!-- source : http://github.com/gdemir/moonmode -->
  <link rel="stylesheet" type="text/css" href="https://barak-framework.github.io/assets/css/moonmode.min.css" />
  <!-- Moonmode end -->

  <script type="text/javascript">

  $(document).ready(function() {

    function get_markdown(URL) {
      $.ajax({
        url: URL,
        type: 'get',
        dataType: 'html',
        async: false,
        success: function(data) { RESULT = data; }
      });
      return RESULT;
    }

    $("#moonmode-logo").click(function() {
      $("body").toggleClass("moonmode-body");
      $("#readme").toggleClass("moonmode-page");
    });

    $("#path").hide();
    $('.page').click(function() {
      var PAGE = $(this).attr('id');
      var MARKDOWN = get_markdown("https://raw.githubusercontent.com/miray-market/miray-market.github.io/master/pages/_" + PAGE );
      var converter = new showdown.Converter();
      var HTML = converter.makeHtml(MARKDOWN);

      var PAGETEXT = $(this).text();
      $("#subpath").html(PAGETEXT);
      $("#path").show()

      $("#readme").html(HTML);

      $('pre code').each(function(i, e) { hljs.highlightBlock(e) });

    });

  });
  </script>

  <style type="text/css">
  /* locals */

  @import  url('https://fonts.googleapis.com/css?family=Nunito:300,400,600');
  body { font-family: 'Nunito', sans-serif;  background-color: #fdfdfd; }
  code { color: #c7254e; }

  #intro { font-size: 12px; color: #777; }
  #intro h3 { margin: 0; padding: 10px; font-size: 33px; font-weight: 300; line-height: 1.1; }
  #intro h5 { margin-top: 20px; margin-bottom: 20px; font-size: 12px; font-weight: 500; }

  #about { border-top: 1px solid #ccc; }

  #readme { color: #333; }
  #readme h1 {
    color: #d3d3d3;
    font-size: 2.5em;
    font-weight: 700;
    height: 130px;
    background-color: rgba(0, 0, 0, 0.6);
    border-radius: 10px;
    text-align:center;
    margin:0em;
    vertical-align:center;
    padding-top:33px;
  }

  #readme h4 { border-bottom: 1px solid #e1e4e8; padding-bottom: 1em; }
  #readme h5 { border-radius: 8px; border: 2px dotted #424242; padding: 1em; }

  .turquoise_color { color: turquoise; }
  .turquoise_border { border:3px solid turquoise; border-radius: 8px; }

  /* overwrite TurkuazCSS */

  blockquote { background-color: transparent; }
  ol, ul, dl { list-style-type: disc; }
  </style>
</head>
<body style="background-color:#eee">

  <div class="container-fluid">
    <div class="row" style="padding-top:10px">
      <div class="ck6 k6 o6 b6 cb6">
        <a href="http://miray-market.github.io">
          <img src="https://raw.githubusercontent.com/barak-framework/barak-framework.github.io/master/assets/img/default-border.png" height="58">
        </a>
      </div>
      <div class="ck6 k6 o6 b6 cb6" style="margin-top:17px;text-align:right">
        <a href="http://miray-market.github.io">
          Barak Framework
        </a>
      </div>
    </div>
  </div>

  <nav class="menu">
    <div class="container">
      <a href="http://miray-market.github.io">Anasayfa</a>
      <a class="page" id="terms-of-use.md">Kullanım Şartları</a>
      <a class="page" id="privacy-policy.md">Gizlilik Politikası</a>
      <a class="page" id="about.md">Barak Hakkında</a>
    </div>
  </nav>

  <div id="path" style="text-align:right">
    <nav class="konum">
      <ul>
        <li><a href="http://barak-framework.github.io/pages">Ana Sayfa</a></li>
        <li><a id="subpath"></a></li>
      </ul>
    </nav>
  </div>

  <div class="container-fluid">
   
  </div>
    

  <!-- Moonmode logo start -->
  <div id="moonmode-logo" style="bottom:40px; left:40px;"></div>
  <!-- Moonmode logo end -->


  <!-- backtotop start -->
  <!-- source : http://github.com/gdemir/backtotop -->
  <link rel="stylesheet" type="text/css" href="https://barak-framework.github.io/assets/css/backtotop.min.css" />
  <a href="#" id="backtotop" title="Back to top">&uarr;</a>
  <script src="https://barak-framework.github.io/assets/js/backtotop.min.js"></script>
  <!-- backtotop end -->

</body>
</html>
