# How do I make animations work in Internet Explorer <= 9?

You can use IE conditional comments to load JavaScript only in IE

    <!--[if lte IE 9]>
      <script src="ie-fallback.js"></script>
    <![endif]-->