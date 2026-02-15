You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "Srijan Infra & Building Solutions Pvt Ltd | About Us",
      "first_heading": "ABOUT US"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "Srijan Infra & Building Solutions Pvt Ltd | Contact Us",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/5ecf9a22a9fea377b8fd4e5d4a7d1a70.css",
    "context": {
      "path": "css/5ecf9a22a9fea377b8fd4e5d4a7d1a70.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/87b794ec556b63cc51afb001d70fc32a.css",
    "context": {
      "path": "css/87b794ec556b63cc51afb001d70fc32a.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/cd4167fd45d0fb1271c90a20f1a60bfb.css",
    "context": {
      "path": "css/cd4167fd45d0fb1271c90a20f1a60bfb.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/e980cb6b50645ddc9d24377f2fe05d53.css",
    "context": {
      "path": "css/e980cb6b50645ddc9d24377f2fe05d53.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "gallery.html",
    "context": {
      "title": "Srijan Infra & Building Solutions Pvt Ltd | Gallery",
      "first_heading": "GALLERY"
    }
  },
  {
    "path": "imgs/03d2336f85593949e556c4cb6e76574a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0bc35a26c89ae631d203bcfb51a4515c.webp",
    "context": {
      "refs": [
        {
          "alt": "Civil & Infra Projects",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/11a3a7af700e9897235711d9517e7419.webp",
    "context": {
      "refs": [
        {
          "alt": "01",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/137845ca43849c47cb0708a3fd1fd38b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/170e0d2ec112db6d16b944ea51ab81cf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/17d60e5958f22063b15a716480199597.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1b8c768450d585596688783bc2d69ef4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1e60d7db8f975ae24fc10d02aa7d1216.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1eebf0893ab09cbb50816467dcbd1ade.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/242f9ee1f208545eb9bf695cce9a35b0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2dd4b1f2f40ff26660923ef08d5f0622.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/38a6f7821b62964f0cffb132f97069b9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3aec224ec5c35a30ed34bb0fb12a2eb6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3ecc8093ad7d7d3eff5769229612f4d8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4496b6fd68e3801bd98e24eb7c1b0c94.webp",
    "context": {
      "refs": [
        {
          "alt": "01",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/46774ce677cff5eaa68ea2fde9f7cd55.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/482e97d31c6f0dc2fe8133db4d5477dc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4c89cae72dd5e91ce8d4fb5de4da3418.webp",
    "context": {
      "refs": [
        {
          "alt": "Pre-Engineered Building",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4e4a64f34745f592d31ab83409d14135.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4ee2ea00ce90fc96ade96a902e46809e.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "srijanlogo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4f5af9060c53bc71b1045cc4a2193674.webp",
    "context": {
      "refs": [
        {
          "alt": "Pre-Engineered Building",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5195c17cfd50e2e7a06f39b0c988d7be.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/52734116bdfd42434234383cbca2d5b2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/52f93fa7f4fb6755b187130ad9d18175.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5553384f6d3f5a1760ee4ab99d260c24.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5b10f8cc398a512e642e4732fab470a7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5ba78231954748d5973c90d2d11adb78.webp",
    "context": {
      "refs": [
        {
          "alt": "peb",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/60e4d735496f2c8b131242df4ee957ea.webp",
    "context": {
      "refs": [
        {
          "alt": "SiteFabrication",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/646164d48db35be79602306441fc38d8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/650b6825629938269af9507a80ef8329.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/686e87b2b22a0f9e514320dd04fa79fc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/708eb27567205770503339da50dc807f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/752e19302aec50c40caa9f2d83c36655.webp",
    "context": {
      "refs": [
        {
          "alt": "RMC Supply",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7db1b6a3b8cfe2bb36925fa5e4d1fab3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/83d8fd3234f3f9a1e1614c01ed2db0fd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/84ceb44d067eda0143d5813ed4b18e3f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/89084fdd1b23e3da304c2b72357125d0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8943a66d262f848b8aa94e62bbc1f649.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8aa0c7c2d965023fd5a2eb6484012109.webp",
    "context": {
      "refs": [
        {
          "alt": "Civil & Infra Projects",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8e288e83ab6c2c59a6cd0bb5e8518aac.webp",
    "context": {
      "refs": [
        {
          "alt": "peb",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/90973fba244a208394cf75a9282d8f4a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/94801cea04c0543ab82d2c3de52a67ea.webp",
    "context": {
      "refs": [
        {
          "alt": "4",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9f2f268a4548512e19c88fd3ec60e829.webp",
    "context": {
      "refs": [
        {
          "alt": "Turnkey Solution",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a8bfab28cb158702595c17dedecb603d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/add2af86472f7dc69717c502dfd006ff.webp",
    "context": {
      "refs": [
        {
          "alt": "peb",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/af89ed00e1af2d91c9788c845dae06b7.webp",
    "context": {
      "refs": [
        {
          "alt": "peb",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b9200c2789df1b1b0a1863c95778746c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c023d3a2daf0f8b18e1ad5a03aa732cc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cd612d1034e01b86220fe1278a885577.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cee0d6b6fb2a508b51118eb0dfaeb894.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d86b2203d34997bb03312e02e2491e7c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/db8529e58573ae2404b3ab4a7654aaae.webp",
    "context": {
      "refs": [
        {
          "alt": "VISION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e399221f0944052e163074b8526246d5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eebb216d5bc2c00de012a9b5c0fb613e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f14b039b13bc9c7271de8f25ab1823a1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f4955f77666b24cd7fd45c4bee894cc8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f5b82071c1a2e9489e07fc1ddcc5e922.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f5c28fa3416ea51fbbab1674a8478c04.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f710caea201df79fe97964f45b96454d.webp",
    "context": {
      "refs": [
        {
          "alt": "Turnkey Solution",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fed838fa0f6a94be329de1c5b7377955.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Srijan Infra & Building Solutions Pvt Ltd | One stop solution for PEB, Civil & Infra projects",
      "first_heading": "Srijan Infra & Building Solutions"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "services.html",
    "context": {
      "title": "Srijan Infra & Building Solutions Pvt Ltd | Services",
      "first_heading": "SERVICES"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.