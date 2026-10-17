# Amazon Visual and Brand Content: Requirements and Best Practices (as of 17 Oct 2026, US focus)

Source labels: **[AMZ]** = Amazon-owned page or Amazon staff post (confirmed rule or Amazon data). **[PRESS]** = trade press. **[AGENCY]** = agency or vendor blog (opinion or second-hand). Firecrawl was heavily rate-limited, so 5 pages were read in full: sell.amazon.com video blog, Canopy (13 Oct 2026), EcomCrew (Premium A+), and ppc.land (A+ and AI). One eWeek scrape failed. The rest comes from search-result snippets and is marked as such.

## 1. Product images: main image rules, secondary images, slots, and the "6 images + 1 video" tension

### Takeaway
The main image rules are long-standing Amazon rules: a pure white RGB 255,255,255 background, the product filling 85–100% of the frame, no text, logos or props, 500–10,000 px on the longest side, at least 1,000 px for zoom, and JPEG/TIFF/PNG/non-animated GIF. Amazon staff recommend "at least six images and one video". Amazon's own video page says a shoppable video only appears in the main media block if the product has **fewer than six images**. That is a real conflict, and sellers have to choose one or test both.

### Cited Findings
- [AMZ, quoted via agency] Main image requirements, per Amazon staff guidance on the Seller Forums:
  - "pure white (RGB 255, 255, 255)" background
  - product fills "85-100% of the image frame"
  - no "text, graphics, logos, watermarks, or promotional messaging on main images"
  - no props or items that are not included
  - "500 to 10,000 pixels" on the longest side, with ≥1,000 px for zoom
  - formats JPEG, TIFF, PNG, or non-animated GIF
  - [Canopy, 13 Oct 2026](https://canopymanagement.com/amazon-product-images-that-convert/)
- [AMZ forum staff post, via search snippet] Same rules: "Product must fill at least 85% of the image frame". The minimum is 500 px on the longest side, with 1,000 px recommended for zoom. Show "only the product being sold (no illustrations, added text, graphics, watermarks, props or accessories not included in the purchase)". — [Seller Forums](https://sellercentral.amazon.com/seller-forums/discussions/t/13af96ea-6b07-4bf9-8dbe-a13292c2e3b1); [Seller Forums](https://sellercentral.amazon.com/seller-forums/discussions/t/3cd8bb69-073a-4e6e-83f2-42c71cbbde17)
- Conflict on minimum size and file size:
  - Some third-party guides state 1000×1000 px as a *requirement* for the main image. — [SellerSprite](https://www.sellersprite.com/en/blog/Amazon-Image-Requirements-Optimization-Tips)
  - File-size maximum is quoted as 10 MB by a converter-tool blog. The Amazon forum snippet said "10GB", which looks like a typo. Treat the limit as unverified. — [Contenta](https://www.contenta-converter.com/blog/amazon-product-photo-requirements-2026.php)
- [AMZ, via agency] Amazon staff recommend "at least six images and one video". — [Canopy](https://canopymanagement.com/amazon-product-images-that-convert/)
- [AMZ] "For shoppable videos to appear in the main media block of product detail pages, the product must have fewer than six images. The most recently uploaded video gets priority in the display order." The troubleshooting steps repeat it: if a video shows "Published" but is not visible, "verify that there are fewer than six images for that product." — [sell.amazon.com blog](https://sell.amazon.com/blog/amazon-product-video)
- [AGENCY opinion] Canopy's take on the conflict:
  - If the product needs to be seen in motion, keep the gallery at five images so the video stays in the main block.
  - If the product is easy to understand from stills, use all the image slots and treat video as a supporting asset.
  - If unsure, test it.
  - [Canopy](https://canopymanagement.com/amazon-product-images-that-convert/)
- [AGENCY] Slot counts: "you can upload up to 9 pieces of content (images + video)… customers typically only see the first 7 images, or 6 if there is a video." This is not confirmed on an Amazon page in this research. — [SalesDuo](https://salesduo.com/blog/amazon-product-detail-page-images/)
- [AGENCY opinion] Objection-led secondary image sequence, with one objection per image:
  1. Core benefit
  2. Size/scale with dimensions. Size is "behind more 'not as expected' returns than any other detail".
  3. Feature-proof close-up
  4. In-use lifestyle
  5. Top objection from reviews, Q&A and returns (compatibility, care, assembly)
  6. What's in the box
  - Text on secondary images is allowed. Treat each image as a billboard: one idea, few words, readable on a phone.
  - Check the main image on a phone in the search grid. "If you can't tell what it is in two seconds, neither can the shopper."
  - [Canopy](https://canopymanagement.com/amazon-product-images-that-convert/)
- [AMZ forum post] Brand owner priority:
  - Amazon "will prioritize brand owner images" and uses third-party sellers' images only when required images are missing.
  - It started with hardlines and is expanding to softlines and consumables.
  - A detail page needs at least three required images: white background, in-environment, and product information.
  - To remove an incorrect image, sellers contact Selling Partner Support.
  - Canopy dates this to 2024.
  - [Seller Forums (EU)](https://sellercentral-europe.amazon.com/seller-forums/discussions/t/78e196e6-a4d0-431f-aadf-eaaa58513fa8); [Seller Forums (US)](https://sellercentral.amazon.com/seller-forums/discussions/t/9bf72c46-d413-404f-8e28-208ee75d54ee); [Canopy](https://canopymanagement.com/amazon-product-images-that-convert/)
- [AMZ, via agency] Visual search:
  - Lens Live launched September 2025.
  - In June 2026 Amazon added Shop by Style, Visual Suggestions and Circle to Search to Lens.
  - Alexa for Shopping (May 2026) supports photo-based visual search.
  - Canopy advises one clean shot from each real-world angle a shopper might photograph the product from.
  - [Canopy](https://canopymanagement.com/amazon-product-images-that-convert/)
- [AGENCY] Images are not a listed ranking factor. They drive CTR and conversion, and ranking follows sales. — [Canopy](https://canopymanagement.com/amazon-product-images-that-convert/)

### Inferences
- For most products with a strong demo case, the five-image-plus-video configuration is the Amazon-documented way to get video into the main gallery. The "6+1" staff advice and the "<6 images" display rule cannot both be fully met, so a Manage Your Experiments test is the clean way to decide.

### Gaps
- No current Amazon help-page text was read directly on: maximum file size, maximum number of image slots (9 vs. other), or category-specific style guides. Check the Seller Central "Product image requirements" help page.
- No CA/AU differences were found for image rules. They are believed to be the same global rules, but this was not verified.

## 2. Video: eligibility, limits, specs, sales-lift data, vertical, Sponsored Brands video

### Takeaway
Any Professional seller with at least three months of selling history and live listings can upload shoppable videos, Brand Registry or not. The limit is up to 4 per ASIN. Specs are .mov/.mp4, up to 1080p, ≤5 GB, 1–12 minutes. Amazon's internal data (Jan–Jun 2026) shows detail pages that added their **first shoppable video averaged +24% sales**, with higher lifts in some categories. Sponsored Brands video is 6–45 s, 16:9 plus (reportedly) 9:16, ≤500 MB.

### Cited Findings
- [AMZ] Eligibility: "Both brand registered and non-brand registered sellers with at least three months of selling history can add shoppable videos… You'll need a Professional selling account, at least three months of selling history, and live product listings." — [sell.amazon.com](https://sell.amazon.com/blog/amazon-product-video)
- [AMZ] "You can add up to 4 shoppable videos to any ASIN."
  - Amazon reviews each video against community guidelines.
  - Approved videos typically appear within 3 days, or up to 7 business days in holiday seasons.
  - Upload through Catalog > Upload and Manage Videos, or through Image Manager > Videos tab.
  - Video types: Product overview, Unboxing, How-to, Setup, Troubleshooting, Brand story, Other.
  - There is a toggle to include variations.
  - [sell.amazon.com](https://sell.amazon.com/blog/amazon-product-video)
- [AMZ] Specs:
  - .mov or .mp4, resolution up to 1080p, maximum 5 GB, length 1–12 minutes.
  - Thumbnail: .jpg/.png/.gif/.bmp.
  - [sell.amazon.com](https://sell.amazon.com/blog/amazon-product-video)
- Specs conflict: a February 2026 guide says ≤1 GB and <5 minutes. A third-party spec sheet lists 1280×720 minimum, 1920×1080 recommended, 16:9. Amazon's page above is authoritative. — [Spark House](https://thesparkhouse.com/blog/how-to-add-videos-to-amazon-product-listing); [evolveamz](https://evolveamz.com/amazon-product-video-specs-requirements-2026/)
- [AGENCY, unverified] One vendor blog claims "up to five videos per ASIN". This contradicts Amazon's "up to 4". — [search snippet, gotrellis](https://gotrellis.com/resources/blog/how-to-add-videos-to-amazon-product-listing/)
- [AMZ data] "Product detail pages with their first shoppable video added saw an average 24% increase in sales compared to those without videos." The footnote reads "Amazon internal data, January – June 2026". The blog is dated 12 May 2025 but was evidently updated.
  - Category lifts: Toys 32.7%, Apparel 30.5%, Home 26.7%, Beauty 25.8%.
  - [sell.amazon.com](https://sell.amazon.com/blog/amazon-product-video)
- Earlier Amazon figure: 23.8%, from a non-US study of 17 marketplaces, Jan–Jun 2024. — [search summary of sell.amazon.com / UK/FR pages](https://sell.amazon.co.uk/learn/how-to-add-videos-to-product-pages-guide)
- [AGENCY opinion] Front Row:
  - It cites Amazon's "Potential Sales Lift" tool by category: Clothing 29.9%, Beauty 18.3%, Health & Personal Care 17.2%.
  - It argues the true incremental effect is more like 5–10%, because of selection bias (Amazon compares pages that added video with pages that did not).
  - [Front Row](https://www.frontrowgroup.com/en/insights/product-videos-the-missing-step-in-increasing-your-sales)
- [AMZ] Creative guidance:
  - "Most successful videos are just 30 to 90 seconds long and highlight the most important feature in the first 5 to 10 seconds."
  - Use text overlays for sound-off viewing.
  - Pick a thumbnail that shows the key benefit. It is what shoppers see in search.
  - "Authenticity beats perfection." A smartphone is enough.
  - Videos also appear in the below-the-fold videos section and in search results.
  - Videos can be reused across variations and global stores.
  - [sell.amazon.com](https://sell.amazon.com/blog/amazon-product-video)
- [AMZ] A+ Content videos are a separate surface. They need Brand Registry, or a Professional account with generic products. — [sell.amazon.com](https://sell.amazon.com/blog/amazon-product-video)
- [AGENCY opinion] A slideshow of existing photos set to music "adds little". Show what stills can't: how the product moves, folds, attaches, or feels in use. — [Canopy](https://canopymanagement.com/amazon-product-images-that-convert/)
- Sponsored Brands video specs (third-party compilations; no Amazon Ads page was read):
  - Length 6–45 s. Recommendations vary: ≤20 s, or 15–30 s.
  - 1280×720, 1920×1080, or 3840×2160.
  - ≤500 MB, MP4/MOV, H.264/H.265, audio ≥96 kbps.
  - Keep text out of the lower-right corner, where the mute toggle sits.
  - Aspect ratio conflict: some sources say 16:9 only, others list a 9:16 vertical option.
  - [SalesDuo](https://salesduo.com/blog/amazon-sponsored-brand-ads-guide/); [evolveamz](https://evolveamz.com/amazon-product-video-specs-requirements-2026/); [spec PDF aggregator](https://cphere-backend.onrender.com/api/public/creative-specifications/publications/1/platforms/amazon-ads.pdf); [SellerMetrics](https://sellermetrics.app/amazon-sponsored-brand-video/)

### Inferences
- Video is the highest-evidence visual lever Amazon publishes: +24% average for the first video, from Amazon's own data. Read it as an upper-bound, observational figure, not a guaranteed incremental lift.
- For leather goods, the Apparel/Home lift ranges (~27–31%) are the closest category analogues. The closest fit depends on the browse node.

### Gaps
- No Amazon page was found stating 2026 vertical-video rules for detail-page shoppable video. The spec says "up to 1080p" with no orientation rule found.
- Amazon Ads' own Sponsored Brands video spec page was not read, so the 9:16 support is unconfirmed.

## 3. AI-generated images: the synthetic-performer rule, accuracy, Amazon's AI tools, brand-owner priority

### Takeaway
There is no Amazon ban on AI imagery. Two rules apply:
- **Accuracy**: images must represent the actual product.
- **Since late July 2026**, photorealistic AI-generated people in listing images, videos and A+ must be tagged with the XMP/IPTC metadata keyword **`contains-synthetic-performer`** in `dc:subject`. The trigger was New York GBL §396-b.

Amazon ships its own AI image generators, for ads since October 2023 and in A+ Content Manager since November 2025. Brand-owner images are prioritised over reseller images.

### Cited Findings
- [PRESS] The synthetic-performer rule:
  - In late July 2026, Amazon began requiring sellers to tag listing images, videos and A+ content that show photorealistic AI-generated people.
  - The keyword `contains-synthetic-performer` goes in the `dc:subject` XMP field, using an IPTC-compatible editor.
  - Labelling is via embedded file metadata, not titles, file names, alt text or bullets.
  - Qualifying content may get a customer-facing indicator.
  - Legal trigger: New York General Business Law §396-b, effective 9 June 2026, with civil penalties of $1,000 for a first violation and $5,000 for subsequent ones.
  - Exclusions: TV, video game and movie characters, and real people even if AI-altered.
  - [eWeek](https://www.eweek.com/news/amazon-ai-generated-product-images-labels-new-york-law/); [IADS / CNBC-sourced](https://www.iads.org/member/news/amazon-cracks-down-on-use-of-ai-images-by-sellers-after-new-york-law); [Novadata (dates rule to 23 July 2026)](https://novadata.io/resources/news/amazon-sellers-label-ai-generated-people-ny-law-july-23-2026). Content is from search snippets; the eWeek scrape failed.
- [PRESS, low confidence] One less-established outlet says the rule applies marketplace-wide rather than by shopper location. — [beBOLD](https://www.bebolddigital.com/news/amazon-ai-generated-people-label) (per search summary)
- [AMZ, via agency] Canopy on Amazon's position:
  - Accuracy: "ensure images accurately represent your product."
  - Amazon has had an ad image generator since October 2023, and AI image tools inside A+ Content Manager since November 2025.
  - Claims that Amazon "banned AI images" do not trace back to an Amazon source.
  - [Canopy](https://canopymanagement.com/amazon-product-images-that-convert/)
- [AGENCY, unverified] Other Amazon tools reported by agencies:
  - A free AI tool ("Canvas") that generates lifestyle images from one product photo.
  - A Seller Central image-generation feature whose outputs are said to be usable in secondary slots.
  - "Gen AI Listing", "Gen AI A+ Content" and Creative Hub tools.
  - No Amazon launch notice was found.
  - [WebProNews](https://www.webpronews.com/amazon-bets-big-on-ai-generated-product-images-challenging-sellers-to-rethink-how-they-sell-online/); [Seller Labs](https://www.sellerlabs.com/knowledge-base/generating-product-images-and-lifestyle-shots-with-ai-whats-allowed/); [Nexscope](https://www.nexscope.ai/blog/free-official-amazon-ai-tools)
- [AGENCY opinion] "Photograph the real product, use AI for context, and check every final image against a physical unit." AI-generated *products* cause mismatches, such as a wrong handle, finish or strap, which drive returns and "doesn't look like the picture" reviews. — [Canopy](https://canopymanagement.com/amazon-product-images-that-convert/)
- [AMZ forum] Brand owner image priority: see Section 1. — [Seller Forums](https://sellercentral.amazon.com/seller-forums/discussions/t/9bf72c46-d413-404f-8e28-208ee75d54ee)
- [PRESS] Related AI-substitution precedent: titles are capped at 75 characters from 27 July 2026, with overflow going to a new "Item Highlights" field of ≤125 characters. Titles not updated are rewritten by Amazon's AI. — [ppc.land](https://ppc.land/amazon-a-content-trains-ai-through-conversions-not-indexing/)

### Inferences
- For a leather brand using AI models wearing or carrying products, the `contains-synthetic-performer` tag is mandatory practice for any photoreal AI person. Leather texture, colour and grain must match the physical unit, or returns and reviews will suffer.

### Gaps
- The original Amazon Seller Central announcement of the synthetic-performer rule was not read directly.
- No evidence was found of a rule letting Amazon *replace* a brand owner's own images with AI-generated ones. The closest documented cases are brand-owner prioritisation, AI-written alt text, and AI title rewrites.
- CA/AU applicability of the synthetic-performer rule is unclear. Reports say "worldwide stores".

## 4. A+ Content: Basic vs Premium, modules, limits, rejections, indexing, alt text

### Takeaway
Since **May 2026**, Premium A+ appears to be enabled for all Brand-Registered Seller Central brand owners at no cost. Two A+ Content Manager notifications announced this, and a "Content Quality Analysis" score launched alongside it. Some June 2026 sources still describe the old gate (Brand Story on every ASIN plus 5 approved A+ submissions in 12 months), so verify in-account.

Module counts:
- Basic: up to 5 modules from a library of 14, images up to 970×300.
- Premium: up to 7 modules from a library of 19, images up to 1464×600, with video, hotspots, carousels, enhanced comparison charts and Q&A.

A+ body text is broadly reported as *not* indexed for keyword ranking. Seller-written alt text is being removed and replaced with AI-generated alt text. This is confirmed in Europe; US status is unconfirmed in sources found.

### Cited Findings
- [Notifications quoted by trade press]
  - Two notifications appeared in A+ Content Manager in May 2026: "Premium A+ is now available to all Seller Central Brand Owners, and you'll continue to have full access to all Premium features."
  - A second introduced the beta Content Quality Analysis score.
  - Previously, Brand Story on every ASIN and a minimum number of approved A+ projects were required. The article calls "that barrier… now gone".
  - [EcomCrew, 15 Jun 2026](https://www.ecomcrew.com/amazon-premium-a-content-is-now-free-for-all-brand-registered-sellers/)
  - First reported 18 May 2026, with notifications seen 21 May 2026. — [My Amazon Guy](https://myamazonguy.com/news/amazon-premium-a-content-free-for-all-sellers/); [Novadata](https://novadata.io/resources/news/amazon-premium-a-plus-default-quality-score-may-2026)
- Conflict: ppc.land, 22 June 2026 (citing ZonGuru), still describes the gate:
  - Professional account, Brand Registry, a published Brand Story on every brand-owned listing, and **five approved A+ project submissions in the trailing 12 months**. One page counts as one submission. The old 15-submission threshold is outdated.
  - Access is granted automatically via a banner.
  - Titan Network also lists Brand Registry + 5 Basic projects + Brand Story.
  - [ppc.land](https://ppc.land/amazon-a-content-trains-ai-through-conversions-not-indexing/); [Titan Network](https://titannetwork.com/amazon-a-plus-content-guide/)
- [PRESS, citing A+ Design Guide] Module limits:
  - Basic: up to 5 modules from a library of 14, images up to 970×300.
  - Premium: up to 7 modules from a library of 19, images 1464×600, plus interactive hotspots, multiple video modules and enhanced comparison charts.
  - [ppc.land](https://ppc.land/amazon-a-content-trains-ai-through-conversions-not-indexing/)
- [AMZ claims, via press] Basic A+ "can lift sales up to 8%". Premium A+ up to 20%. No methodology is given. — [ppc.land](https://ppc.land/amazon-a-content-trains-ai-through-conversions-not-indexing/); [EcomCrew](https://www.ecomcrew.com/amazon-premium-a-content-is-now-free-for-all-brand-registered-sellers/)
- [AGENCY, unsourced] "Standard A+ drives 5-10% conversion lifts… Premium 15-20%… both reduce return rates by 10-15%" (Sequence Commerce, cited by EcomCrew). — [EcomCrew](https://www.ecomcrew.com/amazon-premium-a-content-is-now-free-for-all-brand-registered-sellers/)
- [PRESS] Premium modules: full-width layouts up to 1,464 px, video carousels, interactive hotspots, image carousels, enhanced comparison tables, Q&A modules. — [EcomCrew](https://www.ecomcrew.com/amazon-premium-a-content-is-now-free-for-all-brand-registered-sellers/)
- [PRESS] A+ Content Manager changes on 22 Feb 2026:
  - Shoppable Collections Beta ended 27 Feb 2026, replaced by Brand Story.
  - Content Quality Analysis beta launched. It scores pages weekly on readability, information completeness, visual presentation and conversion effectiveness.
  - EcomCrew describes the score as being about completeness, image quality and module mix.
  - [ppc.land](https://ppc.land/amazon-a-content-trains-ai-through-conversions-not-indexing/); [EcomCrew](https://www.ecomcrew.com/amazon-premium-a-content-is-now-free-for-all-brand-registered-sellers/)
- [PRESS/AGENCY] Rejection triggers:
  - Promotional or pricing claims, competitor mentions, contact info, external links/URLs, and unsupported claims.
  - Warranty language, shipping promises, time-sensitive copy, watermarks, low-resolution images, and third-party logos.
  - Rejection is flagged per module.
  - Approval typically takes 3–7 business days.
  - [EcomCrew](https://www.ecomcrew.com/amazon-premium-a-content-is-now-free-for-all-brand-registered-sellers/); [Anglera](https://www.anglera.com/glossary/amazon-a-plus-content); [WisePIM](https://wisepim.com/guides/amazon-a-plus-content); [SellerSprite](https://www.sellersprite.com/en/blog/how-to-create-high-converting-amazon-product-pages-with-a-plus-content)
- Indexing:
  - EcomCrew: "A+ Content text is not indexed for Amazon search ranking."
  - ppc.land/ZonGuru: no Amazon engine has been confirmed to read A+ body text, and agency split-tests agree it doesn't move keyword ranking. The only Amazon staff statement on record says image alt text "helps your products in search results".
  - Google does index A+ text on the rendered page.
  - Keep the hidden backend Product Description field maintained after A+ goes live. Practitioner consensus is that it is still indexed.
  - Contrary opinion: My Amazon Guy claims Amazon does index A+.
  - [EcomCrew](https://www.ecomcrew.com/amazon-premium-a-content-is-now-free-for-all-brand-registered-sellers/); [ppc.land](https://ppc.land/amazon-a-content-trains-ai-through-conversions-not-indexing/); [My Amazon Guy](https://myamazonguy.com/a-content/amazon-indexes-a-content/)
- Alt text removal:
  - Seller-written alt text is being removed from A+ modules and Brand Story in a phased rollout from 2025 through 2026. AI generates the descriptions, including backfilling Brand Story assets.
  - Full removal in Europe. The US is "not yet" per earlier reports.
  - There was no Amazon announcement.
  - Alt text was removed from comparison charts in April 2025.
  - [ppc.land](https://ppc.land/amazon-a-content-trains-ai-through-conversions-not-indexing/); [EcomCrew](https://www.ecomcrew.com/amazon-closes-a-long-standing-seo-loophole-in-a-content/); [My Amazon Guy](https://myamazonguy.com/news/amazon-alt-text-removed-from-indexing/); [ZonWizard](https://www.zonwizard.com/blog/amazon-removes-alt-text-from-images-what-changes-for-your-seo/)
- [AGENCY opinion] Best practices:
  - Lead with the shopper's primary objection, not the brand story.
  - Build comparison charts for variation catalogs.
  - Keep video modules under 60 s, front-loading the first 10 s.
  - Fill the Q&A module from reviews and customer messages.
  - Measure SKU-level conversion before and after publish over ≥30 days.
  - Start with the highest-traffic ASINs.
  - [EcomCrew](https://www.ecomcrew.com/amazon-premium-a-content-is-now-free-for-all-brand-registered-sellers/)
- [AGENCY opinion, ZonGuru via ppc.land] A+ influences Amazon's AI (the COSMO knowledge graph behind Alexa for Shopping) through conversions: search-buy and co-buy pairs. Use lifestyle scenes for use-contexts, comparison charts for is_a/used_as, and Brand Story for audience fit. — [ppc.land](https://ppc.land/amazon-a-content-trains-ai-through-conversions-not-indexing/)
- [AGENCY] A+ images are not bound by the white-background rule but must be accurate. A+ requires Brand Registry. — [Canopy](https://canopymanagement.com/amazon-product-images-that-convert/)

### Inferences
- Treat A+ as a conversion and returns lever, not an SEO lever. Keep keywords in the title, bullets, backend terms and the hidden description.
- Because alt text is being automated, put legible benefit text in the images themselves.

### Gaps
- The "April 2026 removal of seller-editable alt text" was **not** confirmed for the US in any source found. Sources describe EU full removal and an ongoing phased global rollout, plus an April 2025 comparison-chart change. Check the US A+ Content Manager directly.
- No Amazon page was read giving exact per-module text character limits. Commonly cited agency figures were not verified here.
- The Premium eligibility conflict (fully open vs. 5 submissions + Brand Story) remains unresolved by a primary Amazon page.
- No CA/AU-specific Premium A+ rollout information was found.

## 5. Brand Story

### Takeaway
Brand Story is a carousel band that sits above A+ Content. It applies across the brand's ASINs. In February 2026 it auto-replaced the retired Shoppable Collections. Historically, publishing it on all ASINs was a Premium A+ prerequisite; that may no longer apply after May 2026. Exact specs vary across sources.

### Cited Findings
- [AGENCY] Background card size:
  - 1464×625 px is the commonly cited desktop size.
  - Mobile is quoted as 463×625 (eStore Factory) or 463×325 (NLC).
  - Goat Consulting says the 2026 hero background is 3000×600, and that 1464×625 still displays but smaller.
  - [eStore Factory](https://www.estorefactory.com/amazon-guide/what-are-the-amazon-brand-story-modules/); [NLC](https://help.nlc.com/en/articles/11122577-amazon-brand-story); [Goat Consulting](https://www.goatconsulting.com/blog/amazon-brand-story)
- [AGENCY] Text and image limits:
  - Headline ≤30 characters, body ≤135 characters per card.
  - Logo is quoted as a 315×145 minimum (Titan) or 463×625 (Amalyze).
  - ASIN feature images 362×453 (Amalyze).
  - [Titan Network](https://www.titannetwork.com/amazon-brand-stories-elite-seller-guide/); [Amalyze](https://amalyze.com/resources/guides/listing/amazon-listing-pdp-brand-story)
- [AGENCY conflict] Card count is quoted as up to 7 modules (Goat), up to 4 tiles (Amalyze), and up to 19 (NLC). This is unresolved. — sources as above
- [PRESS] Brand Story replaced Shoppable Collections on 27 Feb 2026. — [ppc.land](https://ppc.land/amazon-a-content-trains-ai-through-conversions-not-indexing/)
- [PRESS] Former Premium gate: "Brand Story published across every ASIN". Many sellers were blocked by a single ASIN missing it. Reportedly removed in May 2026. — [EcomCrew](https://www.ecomcrew.com/amazon-premium-a-content-is-now-free-for-all-brand-registered-sellers/); contrast [ppc.land](https://ppc.land/amazon-a-content-trains-ai-through-conversions-not-indexing/)
- [AGENCY opinion] Brand Story carries audience-fit claims (who it is for, brand origin). Amazon's design guide cites Jackery's Brand Story as an example. — [ppc.land](https://ppc.land/amazon-a-content-trains-ai-through-conversions-not-indexing/)

### Gaps
- No Amazon help page with authoritative Brand Story dimensions and card limits was read.

## 6. Brand Store

### Takeaway
A Store requires Brand Registry. Amazon's own figures:
- New-to-brand shoppers who visited a Store were 62.7% more likely to purchase.
- Stores updated in the last 90 days show higher attributed sales per visitor (reported as +35%).

Store Insights shows Overview, Traffic, Engagement, Sales, Pages and Sources. Section-level analytics were reportedly added in January 2026.

### Cited Findings
- [AMZ] New-to-brand shoppers who visited a Brand Store were 62.7% more likely to purchase than those who did not. The data is undated. — [Amazon Ads Stores best practices](https://advertising.amazon.com/library/guides/stores-best-practices) (via search summary)
- [AGENCY citing Amazon 2024 internal data] Stores updated within the last 90 days have 35% higher attributed sales per visitor. — [Pacvue](https://pacvue.com/?p=1754) (via search summary)
- [AGENCY] Store Insights:
  - Tabs: Overview, Traffic, Engagement, Sales, Pages, Sources.
  - Page views show the next day; attributed units and sales after about 2 days.
  - Section-level Store analytics shipped in January 2026.
  - [Intentwise](https://www.intentwise.com/blog/explained-what-is-amazon-brand-store-insights); [Canopy store guide](https://canopymanagement.com/amazon-brand-store-optimization/) (via search summary)
- [AGENCY opinion] A Store has four jobs: merchandise the catalog, convert campaign traffic, build trust, and generate learning from Store Insights. — [Canopy](https://canopymanagement.com/amazon-brand-store-optimization/)
- [AGENCY] A pending trademark application is enough for Brand Registry and Store eligibility. — (search summary; [Eva](https://eva.guru/blog/create-amazon-brand-store/))
- [AGENCY, unverified] ATTN claims "2.3x higher conversion" plus eye-tracking stats. These have no verifiable origin, so do not use them. — [ATTN](https://www.attnagency.com/blog/amazon-brand-store-visual-merchandising-optimization-2026)

### Inferences
- A sensible build is one page per product line (e.g., wallets, belts, bags), with Sponsored Brands pointed at the matching subpage rather than the homepage. This is common agency practice; no Amazon 2026 document was found confirming the lift.

### Gaps
- No Amazon source was found quantifying Sponsored Brands → Store subpage versus product-collection performance. The "store pages per product line" advice is agency practice only in this research.

## 7. Manage Your Experiments (MYE)

### Takeaway
MYE requires:
- the Brand Representative role in Brand Registry
- a Professional plan
- enough recent traffic on the ASIN (Amazon doesn't publish the threshold; eligible ASINs are shown in the tool)

It tests main/product images, titles, bullets, descriptions and A+ Content, plus multi-attribute tests. Typical tests run 8–10 weeks. Test the main image first.

### Cited Findings
- [AMZ help, via search summary] Experiment types include Product Title and Product Images, among others. The eligible ASINs are listed when you create an experiment. — [Seller Central help: Creating experiments](https://sellercentral.amazon.com/help/hub/reference/external/YZYA77YZTWTF7YZ)
- [AGENCY citing Amazon] MYE covers images, titles, bullets, descriptions and A+.
  - It requires a Brand Representative role, a Professional plan, and enough traffic.
  - "Amazon's guidance puts a typical test at 8 to 10 weeks."
  - Test the main image first, change one variable per test, then test the top-objection image.
  - [Canopy](https://canopymanagement.com/amazon-product-images-that-convert/)
- [AGENCY] Duration advice ranges from 4–8 weeks to 10 weeks. One 2026 guide cites a 1,000-session-per-variant floor and 90% confidence, unverified. A Multi-Attribute test (title + images + bullets) exists. — [Seller Labs](https://www.sellerlabs.com/knowledge-base/manage-your-experiments-a-b-testing-listings-the-right-way/); [evolveamz](https://evolveamz.com/amazon-manage-your-experiments-ab-testing-2026/); [GorillaROI](https://www.gorillaroi.com/blog/amazon-ab-testing-split-test-with-manage-your-experiment)
- [AGENCY] Use MYE to A/B test A+ module layouts on high-traffic ASINs after the first publish. — [EcomCrew](https://www.ecomcrew.com/amazon-premium-a-content-is-now-free-for-all-brand-registered-sellers/)

### Inferences
- Best first tests, in priority order:
  1. Main image (angle, fill, pack count)
  2. 5 images + main-block video vs. 6+ images
  3. A+ variant (lead with objection vs. lead with brand)

### Gaps
- No Amazon page stating the exact traffic threshold or the default test-duration options was read.

## 8. Listing-quality scoring of images and A+

### Takeaway
Amazon's current measure is reportedly the **Listing Quality Indicator**, with bands Poor, Fair, Good, Great and Optimized, not a public 0–100 image score. A+ has its own **Content Quality Analysis** score (beta, from February/May 2026). **No Amazon-published numeric image-score threshold was found.**

### Cited Findings
- [AGENCY] The current measure in the "Enhance Listings" experience is the Listing Quality Indicator, with bands Poor / Fair / Good / Great / Optimized. — [SalesDuo](https://salesduo.com/blog/amazon-listing-quality-score-guide/) (via search summary)
- [Vendor] SellerApp's LQI bands (>80 good, <60 poor) are the vendor's own, not Amazon's. — [SellerApp](https://sellerapp.com/help/?p=2191)
- [Low reliability] Novadata claims a July 2026 dashboard rollout that includes an "Image Quality Score". This is unconfirmed. — [Novadata](https://novadata.io/resources/news/amazon-listing-quality-dashboard-rollout-july-2026)
- [PRESS] A+ Content Quality Analysis:
  - Weekly scoring on readability, information completeness, visual presentation and conversion effectiveness.
  - Described as about completeness, image quality and module mix, not keywords.
  - [ppc.land](https://ppc.land/amazon-a-content-trains-ai-through-conversions-not-indexing/); [EcomCrew](https://www.ecomcrew.com/amazon-premium-a-content-is-now-free-for-all-brand-registered-sellers/)

### Gaps
- No Amazon-published image score thresholds were found. Do not quote numeric thresholds as Amazon rules.

## 9. 360 / 3D (supplementary)

### Cited Findings
- [AMZ forum] From 14 Dec 2023, requests to upload 360° images are no longer accepted. Brand owners in the US, UK, DE, ES, FR and IT can upload 3D models instead. — [Seller Forums (EU)](https://sellercentral-europe.amazon.com/seller-forums/discussions/t/bc3d775e-2083-485f-8d87-9b1147df7bd9) (via search summary)
- [Vendor, commercial interest] 3D model specs and process:
  - GLB format: <5 MB, <20,000 triangles, textures ≤1024×1024.
  - Brand Registry only; review takes about 2 weeks.
  - One GLB powers View in 3D and View in Your Room.
  - The 360° experience was removed from detail pages around 20 Jan 2025.
  - [CGIFurniture](https://cgifurniture.com/blog/amazon-3d-product-view-360-vs-ar/)

### Gaps
- No CA/AU 3D availability was found. The Amazon post lists only US/UK/DE/ES/FR/IT.
