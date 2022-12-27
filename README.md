# ScrollTracker
//Simple JS code to display scroll position in px and create a value to track distance a user scrolls.


<div id="value"></div>

      <script>
        let currentValue = 0;
        let currentScrollPosition = 0;

        function updateValue() {
          let scrollPosition = window.scrollY;
          if (scrollPosition - currentScrollPosition >= 100) {
          currentValue += 1;
          currentScrollPosition = scrollPosition * currentValue / 100;
        }
        document.getElementById("value").innerHTML = currentValue;
        }
        window.addEventListener("scroll", updateValue);

        </script>
