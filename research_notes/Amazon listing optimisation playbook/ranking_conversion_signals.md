# Amazon Ranking and Conversion Signals Beyond Listing Text (US, as of 2026-10-17)

Evidence labels used throughout:
- **[AMAZON]** Amazon's own page, policy, or announcement (strongest)
- **[TRADE]** Trade press reporting on Amazon announcements (good, but second-hand)
- **[AGENCY]** Agency or tool-vendor blog (opinion or anecdote; most of these sell services)
- **[ACADEMIC]** Peer-reviewed or preprint research

Source note: EcommerceBytes has stopped publishing. Its site now shows a closing notice after 27 years, so links to its articles no longer load ([ecommercebytes.com](https://www.ecommercebytes.com/qcwe)). Firecrawl rate limits held direct scrapes to 6 pages. Some Amazon help pages, such as the Brand Referral Bonus page, could not be read. Those gaps are flagged below.

## 1. A9/A10 ranking factors: relevance, CTR, conversion, velocity, PPC vs organic, external traffic

### Takeaway
Amazon has never published a ranking formula. The terms "A9" and "A10" come from vendors, not from Amazon. Amazon Science work and job postings confirm that ranking is a machine-learned model that weighs purchase likelihood together with query relevance and personalization. The idea that clicks, conversion, sales velocity and in-stock status matter is consistent with that. The specific weightings that agencies quote, such as "PPC sales count less than organic" or "A10 rewards external traffic", have no support from Amazon.

### Cited Findings
- [AMAZON/ACADEMIC] Amazon's SIGIR 2016 talk "Amazon Search: The Joy of Ranking Products" says product search moved from several hand-tuned ranking functions with a handful of features to a general machine-learning framework that ranks within categories (learning-to-rank with behavioral features). — [Amazon Science](https://amazon.science/publications/amazon-search-the-joy-of-ranking-products)
- [AMAZON, indirect] Amazon job postings for Search Relevance describe teams that "own the ranking models that decide the order of results on every Amazon search page" and models that "jointly optimize purchase, relevance, and personalization". These postings show direction, not method. — [Applied Scientist II, Search Ranking posting](https://mygwork.com/jobs/amazon-applied-scientist-ii-search-ranking-6248980)
- [AMAZON] Amazon's public ESCI Shopping Queries dataset labels each query–product pair as Exact, Substitute, Complement or Irrelevant. This shows that semantic relevance is modeled separately from behavior. — summarized via [arXiv 2309.01610](https://arxiv.org/pdf/2309.01610)
- [AGENCY] Seller-education sources agree there is "no public ranking equation". The factors they commonly list are relevance, price, availability, sales history, reviews, CTR, conversion rate and sales velocity. If a product is out of stock, its rank may drop or it may disappear from results. — [Stack Influence](https://stackinfluence.com/blog/amazon-algorithm-what-sellers-can-actually-control); [Seller Labs on "A10"](https://www.sellerlabs.com/blog/understanding-amazon-a10-algorithm/); [SellerSonar](https://sellersonar.com/blog/glossary/a9-algorithm/)
- [ACADEMIC] A working paper on 2023 Amazon search data found that in the top five results, where typically four are ads, "neither decreased relevancy nor increased price significantly sways user decisions". In other words, position drives clicks. A related paper found the top-3 most-clicked ads were 17% more expensive and one-third less relevant than the organic results next to them. — [UCL Discovery](https://discovery-pp.ucl.ac.uk/id/eprint/10196133)
- [AGENCY] Velocity Sellers (Sept 2026) treats conversion as a ranking input: "conversion is a ranking input, so a sustained badge on a hero SKU degrades organic position through the ordinary mechanism". This is opinion. — [Velocity Sellers](https://www.velocitysellers.com/2026/09/10/amazon-frequently-returned-item-badge-creative-2026/)
- [AGENCY, unverified] The claim that the algorithm "rewards listings with outside traffic" appears in Brand Referral Bonus marketing posts without any source. — [Nova](https://novadata.io/resources/news/amazon-brand-referral-bonus-external-traffic-2026)

### Inferences
- Treat "A10" as marketing shorthand. The defensible model is relevance gating, meaning the listing must be indexed and semantically matched, followed by a behavioral ranker trained toward purchases. Under that model, CTR, add-to-cart, conversion and units sold per query are the likely levers, along with availability and delivery speed.
- No source distinguishes how a sale weighs by its traffic source (ad, organic or external). Any claim that PPC sales are weighted at some fraction of organic sales is folklore.

### Gaps
- I could not find an Amazon patent or 2024–2026 Amazon Science paper that ranks the importance of specific features. The patent search was not completed within the tool budget.
- I found no official Seller Central page listing ranking factors. The Featured Offer guidance cited by blogs (competitive price, fast/free shipping, delivery certainty, availability) concerns the Buy Box, not search, and I could not verify it first-hand.

## 2. Advertising's effect on organic rank

### Takeaway
The mechanism most practitioners accept is indirect: ads produce sales and clicks on a query, and those behavioral signals feed the organic ranker. The only evidence is vendor case studies with no control groups. I found no independent controlled study and no Amazon statement on it either way. "Ranking campaigns" (exact-match, high-bid, single-keyword pushes) and keyword harvesting from search-term reports are agency practices, not documented Amazon mechanics.

### Cited Findings
- [AGENCY] Tinuiti ran an 18-day test on two ASINs with a one-week baseline and no control. One keyword moved from organic #303 to #53, and Tinuiti concluded that rising organic rank drove organic sales. — [Tinuiti](https://tinuiti.com/?p=6094)
- [AGENCY] Perpetua and the agency Cartograph ran a 30-day experiment on one client. They report a 104% increase in daily organic (non-ad-attributed) sales and 40% higher organic rank. Perpetua sells ad-automation software. — [Perpetua](https://perpetua.io/blog-organic-growth-sponsored-ads/)
- [AGENCY/RESEARCH] Bobsled/Acadia and Analytic Index produced a multi-brand report on ad spend versus sales outcomes that includes "the relationship between Sponsored ads and organic ranking". Only its introduction was retrievable, so its findings are not known. — [Acadia](https://acadia.io/?p=4414); [Analytic Index](https://get.analyticindex.com/amazon-sponsorship-impact)
- [ACADEMIC] An AIES 2024 paper simulated 4,800 searches in four countries. Products with poor organic rank (beyond #100) appear as sponsored results above the top organic results, and these top sponsored products are often costlier and lower quality. Ads let weak products jump the organic queue, but the paper says nothing about whether ads lift organic rank. — [AAAI/AIES](https://ojs.aaai.org/index.php/AIES/article/view/31639); [arXiv 2407.19099](https://arxiv.org/abs/2407.19099)
- [AGENCY] Sponsored Products ads only serve for the offer that holds the Featured Offer (Buy Box). Losing the Buy Box to a reseller therefore also stops the brand's ads. — [Repricer.com](https://www.repricer.com/blog/amazon-buy-box-guide-2026/)
- [TRADE/AGENCY] If a Sponsored Products campaign sends traffic to a listing that has lost its strikethrough reference price, conversion falls and CPA rises even when bids and targeting stay the same. — [EcomCrew](https://www.ecomcrew.com/amazon-cracks-down-on-inflated-discounts-with-new-pricing-rules-starting-april-23/)

### Inferences
- Ads probably help organic rank only to the extent that they generate converting sales on the target query. Ads that do not convert are unlikely to help.
- Sponsored Brands and Sponsored Display mainly serve visibility, defense and retargeting. I found no evidence that either affects organic rank directly.

### Gaps
- I found no Amazon Ads documentation stating whether ad-attributed sales count toward organic ranking.
- I found no independent quantitative estimate of the size of the ads-to-organic effect.
- Keyword-harvesting and Sponsored Brands/Display specifics were not researched in depth because of the tool budget.

## 3. Reviews and ratings

### Takeaway
Star ratings come from a machine-learned weighting, not a simple average. Amazon introduced this in 2015, and it weighs recency, helpful votes and verified purchase. Vine's official US fees are $0 for up to 2 units, $75 for 3–10 and $200 for 11–30 per parent ASIN, with billing deferred. Third-party sources that list "quarterly tiers" are wrong. Incentivized reviews are banned. The Request a Review button is the compliant way to ask.

### Cited Findings
- [TRADE, citing Amazon] In 2015 Amazon replaced the unweighted average with a machine-learned model that weighs review age, helpful votes and verified-purchase status. — [GeekWire 2015](https://www.geekwire.com/2015/amazon-changes-its-influential-formula-for-calculating-product-ratings/)
- [AMAZON forum, second-hand] A Seller Central forum reply points to Amazon help pages that describe star ratings as ML-weighted and include reviewer trustworthiness. — [Seller Forums](https://sellercentral.amazon.com/seller-forums/discussions/t/5a005cb7-77e3-45b1-9c99-9c08802f15da)
- [AMAZON, official page] **Vine, US, current:**
  - Eligibility: a Professional selling account; a Brand Representative or Reseller role on a Brand Registry brand, or generic products; and eligible FBA offers.
  - Product limits: fewer than 30 reviews on the detail page, an image and a description. Adult, digital and bundled products are excluded.
  - Units: up to 30 units per parent product.
  - Enrollment fee per parent product (no extra charge for child products): up to 2 units $0; 3–10 units $75 (CAD 100, GBP 60, EUR 70, JPY 10,000); 11–30 units $200 (CAD 240, GBP 140, EUR 170, JPY 22,000).
  - Billing: "You aren't charged until 30 days after enrollment and after your first review is published. If you don't receive a Vine review within 90 days from the date of enrollment, you aren't charged."
  - Timing: enrollment can happen before launch. Amazon recommends having inventory at FCs at least 3 weeks before launch.
  - Cancellation: possible only before any unit is claimed. After a claim, enrollment can only be stopped, and the product cannot be re-enrolled.
  - Amazon's marketing claims an average sales lift of 30% (internal data) and offers a $200 Vine credit to new sellers who enroll in Brand Registry.
  - Vine is available in US, CA, UK, FR, DE, IT, ES, AU and JP.
  - — [sell.amazon.com/programs/vine](https://sell.amazon.com/tools/vine)
- [AGENCY, conflicting] Some 2026 guides state the billing trigger as "7 days after first review". Ecom Circles describes "Basic $200 / Professional $500 / Advanced $1,000+ quarterly" tiers. Both conflict with Amazon's page and should be treated as wrong. — [SellerSprite](https://www.sellersprite.com/en/blog/amazon-vine-program-sellers); [Ecom Circles](https://ecomcircles.com/blog/amazon-vine-program-2026/); [Nova](https://novadata.io/resources/blog/amazon-vine-program-true-cost)
- [AGENCY] Request a Review: the window is usually given as 4–30 days after purchase/delivery, although one guide says 5–30. A product returned before then is ineligible. The email is standardized and cannot be customized. — [SellerSprite](https://www.sellersprite.com/en/blog/how-get-reviews-amazon); [Printful](https://www.printful.com/uk/blog/how-to-get-reviews-on-amazon); [amzdudes](https://amzdudes.com/how-to-get-reviews-on-amazon-10-proven-strategies/)
- [AGENCY, describing Amazon policy] Amazon prohibits compensation for reviews. That covers free products, discounts, refunds or other rewards, including after a review is posted. Sellers may not ask only for positive reviews or word a request so it implies a rating preference. Offering refunds in exchange for removing a review is also prohibited. — [AMZ Advisers](https://www.amzadvisers.com/amazon-review-policy-explained); [eComEngine (updated Jan 2026)](https://www.ecomengine.com/blog/amazon-review-guidelines)
- [TRADE] "Customers say" AI review highlights: a paragraph generated from review text and labeled as AI-generated, which began as a test with US mobile shoppers (2023) and has since expanded. — [Search Engine Land](https://searchengineland.com/amazon-ai-generated-customer-review-highlights-430693)
- [AGENCY] Sellers cannot edit the "Customers say" paragraph or the "Compare with similar items" table. Velocity Sellers notes the return-rate signal has reportedly been available to Rufus, which was renamed "Alexa for Shopping" in 2026 according to the same agency. — [Velocity Sellers](https://www.velocitysellers.com/2026/09/10/amazon-frequently-returned-item-badge-creative-2026/); [Velocity Sellers price history](https://www.velocitysellers.com/2026/09/28/amazon-price-history-365-days-sellers/)

### Inferences
- Under the ML-weighted rating, recent reviews count more, so review velocity affects the displayed star rating as well as the review count. A steady stream of verified reviews can move a rating faster than its historical average suggests.
- Because "Customers say" is built from review text, recurring complaint themes show up in summary form on the page. Fixing the product or the listing is the only lever on it.

### Gaps
- I did not retrieve Amazon's current Community Guidelines or Seller Central review policy text, and the 4-day versus 5-day window for Request a Review is unresolved.
- I found no reliable data on how review count or velocity weighs directly in search rank.

## 4. Returns: Frequently Returned Item badge, "Customers usually keep this item", VoC/NCX

### Takeaway
The Frequently Returned Item badge (tested since about 2023–2024) was made more prominent in February 2026. Reports put it near the price or buy box, and Amazon now shows alternative products beneath badged listings. The threshold is relative to the category and unpublished. Sellers cannot appeal it; it clears only when the trailing return rate improves. "Customers usually keep this item" is the positive counterpart and is still rolling out. The Voice of the Customer dashboard is the seller's monitoring tool.

### Cited Findings
- [TRADE] UK coverage reports that "from the 16th of February 2026, you'll see a frequently returned item badge on some product listings with higher returns than similar products". — [ChannelX](https://channelx.world/2026/02/amazon-frequently-returned-item-badge/)
- [AGENCY] Reports disagree on whether the February 2026 change landed on the 4th or the 16th. Placement moved "prominently near the buy box". Amazon "began surfacing alternative products beneath badged listings", described as a "similar items customers keep" style module. Velocity calls this module the costliest part, because it redirects paid traffic to competitors. — [Velocity Sellers, Sept 10 2026](https://www.velocitysellers.com/2026/09/10/amazon-frequently-returned-item-badge-creative-2026/)
- [TRADE/AGENCY] Placement is described differently by different sources: beside the price, above the buy box, directly above the bullets in dark red with an icon, or below the reviews. Amazon probably varies it by category and test. Badge copy: "Frequently returned item: Check the product details and customer reviews to learn more about this item." — [Cord Cutters News](https://cordcuttersnews.com/amazon-makes-it-easier-to-know-if-a-product-is-frequently-returned/); [Value Added Resource](https://www.valueaddedresource.net/amazon-frequently-returned-items/); [Fluid Marketplaces](https://www.fluidmarketplaces.com/news-insights/amazon-makes-the-frequently-returned-badge-harder-to-ignore/)
- [AGENCY] The threshold is relative to comparable products in the category, measured as units shipped versus customer-initiated returns over a trailing (reportedly 3-month) window. Reported thresholds run from low single digits in grocery to low double digits in some electronics. Amazon publishes no threshold. — [Velocity Sellers](https://www.velocitysellers.com/2026/09/10/amazon-frequently-returned-item-badge-creative-2026/); [Nova](https://novadata.io/resources/news/amazon-frequently-returned-badge-impact-2026); [Front Row](https://www.frontrowgroup.com/en/insights/what-amazon-frequently-returned-badge-means-for-brands)
- [AGENCY] Removal: there is no dispute path through Seller Support and no exemption for buyer-remorse returns. The badge clears automatically once the rate stays below the category threshold, reportedly for at least about 30 days, with practical recovery taking 4–8 weeks. One source says Amazon itself prompted removal after sustained improvement. — [Velocity Sellers](https://www.velocitysellers.com/2026/09/10/amazon-frequently-returned-item-badge-creative-2026/); [Adverio](https://www.adverio.io/how-to-fix-amazon-frequently-returned-badge/); [Nova](https://novadata.io/resources/news/amazon-frequently-returned-badge-impact-2026)
- [AGENCY, anecdotal] Conversion falls an estimated 20–40% once the badge appears, a figure Velocity calls "directional". Velocity also denies a direct ranking penalty and says the damage to rank comes through lower conversion. — [Velocity Sellers](https://www.velocitysellers.com/2026/09/10/amazon-frequently-returned-item-badge-creative-2026/); [Nova](https://novadata.io/resources/news/amazon-frequently-returned-badge-impact-2026)
- [TOOL] From June 27, 2026, DataHawk tracks the "Frequently Returned" badge as product badge data. — [DataHawk changelog](https://docs.datahawk.co/changelog/2026-06-27-amazon-frequently-returned-badge)
- [TRADE] "Customers usually keep this item" tells shoppers that buyers typically keep the product. It is not on all listings and appears to be rolling out gradually. A seller forum thread reports that one listing with 3,000+ reviews and low returns did not show it, which suggests other criteria also apply. — [Cord Cutters News](https://cordcuttersnews.com/amazon-will-now-tell-you-if-a-product-is-something-buyers-typically-keep-or-something-they-often-return/); [SellersAskSellers](https://sellersasksellers.com/t/how-to-get-customer-usually-keep-this-item-banner-in-the-listing/1490)
- [AGENCY] Monitoring workflow: open Seller Central → Performance → Voice of the Customer for per-ASIN return rate and CX Health (NCX). Then read the FBA Customer Returns report reason codes and buyer comments, usually over 90 days. Velocity reports four codes that dominate on healthy products: Not as described, Didn't match expectations, Wrong size or variant ordered, and Not compatible. It treats all four as listing or creative fixes, specifically scale reference, compatibility statement, what's-in-the-box frame and variant ladder. — [Velocity Sellers](https://www.velocitysellers.com/2026/09/10/amazon-frequently-returned-item-badge-creative-2026/)
- [AGENCY] Seasonality: gifting raises return rates, and December returns land in January, so the risk of crossing the threshold peaks in January. — [Velocity Sellers](https://www.velocitysellers.com/2026/09/10/amazon-frequently-returned-item-badge-creative-2026/)

### Inferences
- For product types where size, color or finish expectations drive returns, the strongest returns levers are accurate dimensions, scale photos, close-ups of finish and color, and clear variant naming.

### Gaps
- I found no Amazon help page or announcement defining the badge thresholds, its removal, or the alternatives module. Every detail on the February 2026 change comes from trade press or agencies, and Marketplace Pulse and ppc.land coverage was not found.
- I found no official definition of NCX thresholds in this research pass.

## 5. Pricing signals: List Price, Typical Price, 365-day price history, coupons/PED/deals

### Takeaway
These rule changes are confirmed through Amazon wording quoted in the trade press:
- **List Price (since April 23, 2026):** shown only when validated, either by a recent offer at another retailer or by purchases of the Featured Offer at that price.
- **Typical Price (since May 18, 2026):** includes promotional sales when the product was below its non-promotional median for more than half of 90 days.
- **Price history:** shoppers can now see 365 days of the lowest daily Featured Offer price.
Fake discounts now remove the strikethrough and stay visible to shoppers for a year.

### Cited Findings
- [TRADE quoting Amazon] From April 23, 2026, a seller's List Price is shown only if "the product has been offered at this List Price at another retailer recently" or "has been purchased by customers as the Featured Offer on Amazon at this List Price". Seller assertion alone is not enough. An unverified List Price is not displayed, so the strikethrough disappears. Amazon's March 2026 guidance warned that artificially high List Prices could disable the display and flag the account. — [EcomCrew](https://www.ecomcrew.com/amazon-cracks-down-on-inflated-discounts-with-new-pricing-rules-starting-april-23/), citing [sell.amazon.com/blog/amazon-list-price](https://sell.amazon.com/blog/amazon-list-price) and [ppc.land](https://ppc.land/amazons-fake-discount-crackdown-list-price-rules-tighten-april-23/)
- [TRADE] Typical Price is the median price customers paid over 90 days, excluding promotions. From May 18, 2026, if the price was below the non-promotional median for more than half of the 90 days, promotional sales count too. Coupons, Buy X Get Y, Subscribe and Save and peak-event pricing are excluded from this recalculation. — [EcomCrew](https://www.ecomcrew.com/amazon-cracks-down-on-inflated-discounts-with-new-pricing-rules-starting-april-23/); [Netpeak](https://netpeak.us/blog/amazon-is-changing-how-your-pet-brand-displays-prices-act-before-may-18/)
- [TRADE] Under the Fair Pricing Policy, misleading reference prices can lead to removal of the Featured Offer or suspension. — [EcomCrew](https://www.ecomcrew.com/amazon-cracks-down-on-inflated-discounts-with-new-pricing-rules-starting-april-23/)
- [AGENCY, unverified] One vendor estimates conversion falls 15–20% when the strikethrough is lost. This is a single vendor's figure. — [Nova](https://novadata.io/resources/news/amazon-reference-pricing-list-price-crackdown-april-2026)
- [AGENCY citing Amazon] Price history:
  - Amazon added a 365-day view in May 2026, alongside the 30- and 90-day views, reached through a "Price history" link next to the price or through Alexa for Shopping.
  - It launched in the US, UK and India.
  - The graph plots the lowest Featured Offer price each day.
  - Amazon says more than 50M customers have used price history since its 2024 launch, and its Sept 14, 2026 Prime Big Deal Days (Oct 6–7) announcement promoted "up to 365 days of pricing insights on hundreds of millions of products".
  - Amazon said it would "align reference pricing" with the price-history graph.
  - — [Velocity Sellers, Sept 28 2026](https://www.velocitysellers.com/2026/09/28/amazon-price-history-365-days-sellers/); [About Amazon](https://www.aboutamazon.com/news/retail/how-to-check-amazon-price-history)
- [AGENCY citing Seller Central help] Prime Exclusive Discounts require a validated reference price. The discount must be at least 5% off the lowest non-promotional price of the last 30 days, 5% off the current price and 5% off the reference price. For event deals, the maximum deal price is set from the reference price, the lowest price across sellers in the last 30 days and the 60-day low. Peak-event prices are removed from the 30- and 60-day lookbacks after the event. Prime Big Deal Days prices will not affect the BFCM maximum deal price. Unadvertised price cuts count as non-promotional prices. — [Velocity Sellers](https://www.velocitysellers.com/2026/09/28/amazon-price-history-365-days-sellers/)
- [GOV] The FTC's Guides Against Deceptive Pricing say a "former price" must be one actually offered in good faith for a reasonably substantial period. — [FTC](https://www.ftc.gov/legal-library/browse/rules/deceptive-pricing)

### Inferences
- A permanent sale removes the strikethrough and lowers the Typical Price. Coupons are excluded from the Typical Price recalculation, so they are now the safer tool for always-on value signaling.
- I found no evidence that coupons or deals affect rank directly. Any rank effect would come through the sales velocity and conversion they generate.

### Gaps
- I did not read the primary Seller Central pages on reference pricing directly. The wording comes from trade press quotes.
- I found no data on badge rendering for coupons and deals or on how deals affect rank.

## 6. External traffic: Brand Referral Bonus, Amazon Attribution, ranking effect

### Takeaway
The Brand Referral Bonus (BRB) pays brand-registered sellers a credit worth on average about 10% of sales driven by tagged non-Amazon traffic, measured through Amazon Attribution tags with a 14-day window. Category rates vary. The common claim that external traffic gets a special ranking boost is unverified. Any rank effect is likely to work through ordinary sales velocity and conversion.

### Cited Findings
- [AGENCY] The BRB averages 10% of qualifying sales and is paid as a credit against future referral fees, not in cash. Attribution uses a 14-day window. Results appear in a weekly report. Sellers set it up through Amazon Attribution, which requires Brand Registry. — [Ecommerce Fastlane](https://ecommercefastlane.com/amazon-attribution-brand-referral-bonus/); [Stack Influence](https://stackinfluence.com/blog/amazon-brand-referral-bonus-rates-setup-and-credits); [SellerMetrics](https://sellermetrics.app/amazon-brand-referral/)
- [AGENCY, conflicting] Category rates are reported as "7% to 30%" in one source and "up to 25%" in another. — [Titan Network](https://titannetwork.com/amazon-referral-bonus/); [SellerMetrics](https://sellermetrics.app/amazon-brand-referral/)
- [AGENCY, unverified] One vendor says "A9 rewards listings with outside traffic", with no source. — [Nova](https://novadata.io/resources/news/amazon-brand-referral-bonus-external-traffic-2026)

### Inferences
- External traffic is economically attractive because the BRB credit offsets referral fees. For ranking, the safe assumption is that it helps only if it converts. Low-intent traffic, such as broad social clicks, can lower the conversion rate.

### Gaps
- Amazon's official Brand Referral Bonus page could not be scraped because of rate limits. The official rate table and terms, including a 12-month new-to-brand bonus, were not confirmed.

## 7. Brand Analytics: Search Query Performance, Top Search Terms, Search Catalog Performance

### Takeaway
Brand Analytics requires a Professional account and a Brand Owner/Representative role on a Brand Registry brand. Search Query Performance (SQP) shows, for the brand's top queries (up to about 1,000), the full funnel of impressions, clicks, cart adds and purchases for both the brand and the market. That makes it the best first-party data for choosing keywords. Top Search Terms gives search frequency rank and the top clicked ASINs per term. Search Catalog Performance gives the same funnel per ASIN.

### Cited Findings
- [AGENCY] Access requires a Professional account and Brand Representative status on a brand enrolled in Brand Registry. Trademark sources conflict on whether a pending or a registered trademark is enough. — [Amplisell](https://www.amplisell.com/blog-post/best-amazon-brand-analytics-reports-that-inform-strategy); [Jarvio](https://jarvio.io/blog/amazon-brand-analytics-guide); [Gorilla ROI](https://www.gorillaroi.com/blog/amazon-brand-analytics)
- [AGENCY] SQP covers the top 1,000 most relevant search queries, with impressions, clicks, cart adds and purchases in one funnel. It has brand and ASIN views. — [Adbrew](https://adbrew.io/blog/search-query-performance); [ClearAds](https://clearadsagency.com/amazon-search-query-performance-guide/)
- [TOOL] Search Catalog Performance is available weekly and monthly at ASIN level. — [DataHawk](https://docs.datahawk.co/help-center/data-reference/amz-brand-analytics-data)
- The dashboards also include Top Search Terms, Market Basket, Repeat Purchase and Demographics. — [Amplisell](https://www.amplisell.com/blog-post/best-amazon-brand-analytics-reports-that-inform-strategy)

### Inferences
- Keyword selection workflow:
  1. Use SQP to find queries where the brand has a low share of impressions but its click or purchase share is at or above impression share. These show relevance that has not yet been rewarded with visibility.
  2. Use Top Search Terms to size demand and see who captures the clicks.
  3. Use Search Catalog Performance to spot ASINs with high impressions but low CTR, which points to main image, price or rating problems rather than text.
- The SQP purchase share on a query is also the most direct first-party measure of whether ads, or any other activity, are building organic position on that query.

### Gaps
- I did not read Amazon's own Brand Analytics help pages. The eligibility details come from third parties.

## 8. Buy Box basics and threats; Brand Registry protection tools

### Takeaway
One offer wins the Featured Offer (Buy Box) on a shared detail page, and only that offer runs Sponsored Products ads. Reports show used and Renewed offers occasionally winning the Featured Offer and being merged onto main detail pages. Brand protection relies on Brand Registry tools: Report a Violation, Transparency serialization and Project Zero self-service removal. These were not confirmed in this research pass.

### Cited Findings
- [AGENCY] The commonly cited Featured Offer factors are competitive total price, fast and free shipping, delivery certainty, order experience and availability. The Buy Box holder is the only seller whose Sponsored Products ads serve. — [Repricer.com 2026 guide](https://www.repricer.com/blog/amazon-buy-box-guide-2026/); [Stack Influence](https://stackinfluence.com/blog/amazon-algorithm-what-sellers-can-actually-control)
- [AMAZON forum, anecdotal] Sellers report used offers winning the Featured Offer after price increases. Another thread complains that used offers shown as the Featured Offer drive high returns and dissatisfaction. — [Seller Forums 1](https://sellercentral.amazon.com/seller-forums/discussions/t/9f779828-f6fb-4eae-8d6f-70c01de80077); [Seller Forums 2](https://sellercentral.amazon.com/seller-forums/discussions/t/a26b3ff0-5a29-4ced-8747-d44ddfe69810); [SellerEngine](https://sellerengine.com/used-offers-now-buy-box/)
- [AMAZON forum] Renewed "Refurbished – Excellent" offers for electronics are to be merged onto main detail pages alongside new and used offers. — [Seller Forums](https://sellercentral.amazon.com/seller-forums/discussions/t/088a6c38-ff86-4c35-86d5-661aa30bfde5)
- [AGENCY] Amazon Resale (formerly Warehouse) lists returned units independently, so brands have limited control. — [Be Bold Digital](https://www.bebolddigital.com/blog/what-are-amazon-warehouse-deals)
- [AGENCY] The Featured Offer price is what the price-history graph plots. A cheap reseller or used offer that wins the Featured Offer can therefore pull down the brand's Typical Price and 365-day chart. — inferred from [Velocity Sellers](https://www.velocitysellers.com/2026/09/28/amazon-price-history-365-days-sellers/) ("the graph shows the lowest Featured Offer price each day")

### Inferences
- A used or resale offer winning the Featured Offer has several knock-on effects: the brand's ads stop, the plotted price and Typical Price go down, and the return rate may rise, all of which feed back into the signals above.

### Gaps
- I found no 2026 Amazon documentation in this pass on Transparency (per-unit serialized codes), Project Zero (eligibility and self-service removal) or Report a Violation workflows. These need a separate lookup of Brand Registry help pages.
- I found no confirmed 2026 policy change on used or resale offers on brand listings. The evidence is forum anecdote only.
