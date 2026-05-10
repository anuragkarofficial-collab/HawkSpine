(function () {
    function injectBanner() {
      if (document.getElementById('hawkspine-promo-banner')) return;
  
      var lang = (document.documentElement.lang || 'en').toLowerCase();
      var isFR = lang.startsWith('fr');
  
      var content = isFR
        ? {
            text: 'Obtenez <strong>20 %</strong> de réduction en appliquant le code promo <strong>"HAWKSPINE20"</strong> lors du paiement de votre HawkSpine',
            btn: "J'en profite",
            href: 'https://hawkspine.hawkcell.com/stripefr',
            validity: 'Offre valable jusqu’au 31 mai 2026'
          }
        : {
            text: 'Get <strong>20%</strong> off by applying the promo code <strong>"HAWKSPINE20"</strong> at checkout on your HawkSpine',
            btn: 'REDEEM NOW',
            href: 'https://hawkspine.hawkcell.com/stripe',
            validity: 'Offer Valid till 31 May, 2026'
          };
  
      var wrapper = document.createElement('div');
      wrapper.id = 'hawkspine-promo-banner';
      wrapper.innerHTML =
        '<div class="hawkspine-promo-banner-inner">' +
          '<div class="hawkspine-promo-banner-content">' +
            '<span class="hawkspine-promo-banner-text">' + content.text + '</span>' +
            '<a href="' + content.href + '" class="hawkspine-promo-banner-button" target="_self">' + content.btn + '</a>' +
            '<span class="hawkspine-promo-banner-validity">' + content.validity + '</span>' +
          '</div>' +
        '</div>';
  
      var nav = document.querySelector('nav');
      if (nav && nav.parentNode) {
        nav.parentNode.insertBefore(wrapper, nav.nextSibling);
      } else {
        document.body.insertBefore(wrapper, document.body.firstChild);
      }
    }
  
    if (document.readyState === 'loading') {
      document.addEventListener('DOMContentLoaded', injectBanner);
    } else {
      injectBanner();
    }
  })();
