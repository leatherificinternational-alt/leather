# Amazon Listing Text and Catalog Data: Rules and Best Practices (as of 17 Oct 2026)

Source labels used below:
- **[AMAZON]**: an Amazon help page, a Seller Forums post by Amazon staff (News_Amazon or a moderator), or the SP-API changelog. Sometimes only quoted through trade press; this is flagged as "via".
- **[PRESS]**: trade press (ppc.land, EcomCrew).
- **[VENDOR OPINION]**: an agency or tool-vendor blog or practitioner commentary.

Method note: firecrawl_scrape was heavily rate-limited because the quota is shared. Seller Central help pages G23501 (search terms) and G200390640 (Product detail page rules) could not be scraped. Rules from those pages are therefore taken from search snippets or quoted through secondary sources, and are marked as such. EcommerceBytes has ceased publication, so its archive URLs now redirect to a shutdown notice ([ecommercebytes.com](https://www.ecommercebytes.com/2026/08/07/amazons-new-product-title-policy-also-applies-to-its-listings/)).

---

## 1. Titles: the 75-character limit, style rules, and Item Highlights

### Takeaway
Since 27 July 2026, titles (`item_name`) in every category except media must be 75 characters or fewer, including spaces [AMAZON, via press]. Amazon's AI is gradually rewriting titles that are still over the limit. Brand owners get 14 days to review each rewrite in "Review Listings Changes". The overflow goes into a new **Item Highlights** field (`title_differentiation`, up to 125 characters). That field is searchable and, by Amazon's FAQ, weighted the same as the title. The January 2025 style rules still apply: banned special characters, no word used more than twice, and no promotional terms.

### Cited Findings
**Confirmed Amazon rules (with dates)**
- Announcement posted on Seller Forums by News_Amazon and updated 10 June 2026: titles in all categories except media must be 75 characters or fewer including spaces. After 27 July 2026, listings over the limit are "gradually" updated to the AI recommendation, and listings stay active throughout. — [ppc.land, 13 Jun 2026, quoting the Seller Forums announcement](https://ppc.land/amazon-cuts-product-title-limit-to-75-characters-on-july-27/) ([forum thread](https://sellercentral.amazon.com/seller-forums/discussions/t/145b6d0f-999c-4555-896c-c694bda2e470))
- Amazon quote: "when changes are made to your listings, brand owners will have 14 days before implementation to review, modify, and approve AI-generated recommendations for titles and Item Highlights in Review Listings Changes." ppc.land reads this as covering Brand Registry owners only. — [ppc.land](https://ppc.land/amazon-cuts-product-title-limit-to-75-characters-on-july-27/)
- AI title and Item Highlights recommendations are available in Manage All Inventory under "View enhancements" on any listing. Amazon describes them as automatically meeting the new limits. — [ppc.land](https://ppc.land/amazon-cuts-product-title-limit-to-75-characters-on-july-27/)
- According to Amazon, Item Highlights is meant for materials, recommended use cases and comparison terms. It is searchable and shown alongside the title in search results and on the detail page. — [ppc.land](https://ppc.land/amazon-cuts-product-title-limit-to-75-characters-on-july-27/)
- Amazon's stated reasons for the limit: titles display in full on mobile, and the length matches other online retailers. — [ppc.land](https://ppc.land/amazon-cuts-product-title-limit-to-75-characters-on-july-27/)
- SP-API changelog, 1 July 2026: `item_name` takes up to 75 characters. The new `title_differentiation` attribute (Item Highlights) takes up to 125 characters and **can only be used once `item_name` is 75 characters or fewer**. The change applies to all marketplaces except Saudi Arabia, Egypt, Turkey and the UAE. Existing listings are not touched until an update is submitted. — [SP-API changelog](https://developer-docs.amazon.com/sp-api/changelog/sp-api-updates-eu-fbm-requirements-product-type-definitions-api-title-structure-external-fulfillment-api-shipment-status) via [SoldScope](https://www.soldscope.com/blog/amazon-item-highlights-desktop-august-10)
- Amazon FAQ and forum post as relayed by SoldScope:
  - From **10 August 2026**, Item Highlights display beneath the Item name on desktop as well as mobile.
  - "Item name and Item highlights both feed search, and neither ranks above the other."
  - AI updates continue "through the rest of 2026".
  - Listings that have not been edited stay live, editable and searchable.
  - Best practice is to keep the brand in the Item name.
  - The most important variation attributes go in the Item name, with the rest in Item Highlights.
  - Item Highlights should not repeat the title.
  - More than 984 million titles had been updated since June.
  — [SoldScope (vendor, quoting Amazon forum post)](https://www.soldscope.com/blog/amazon-item-highlights-desktop-august-10) ([forum](https://sellercentral.amazon.com/seller-forums/discussions/t/302aaac6-6f2b-4d86-bcd2-36fe24f0e6cd))
- Enforcement date conflict: most sources give 27 July 2026. Some secondary sources say enforcement slipped to 3 August 2026, citing EcommerceBytes, which is now offline. I could not verify this. — [search summary of amzprep / Canopy / ecommercebytes results](https://amzprep.com/2026/amazon-august-updates/); [Canopy](https://canopymanagement.com/amazon-75-character-title-limit-item-highlights/)
- The previous rule, effective 21 January 2025, capped titles at 200 characters including spaces for most categories. — [Amazon Seller Forums announcement](https://sellercentral-europe.amazon.com/seller-forums/discussions/t/3781c84d-4778-40fe-9dde-30039a0948f6); [ppc.land](https://ppc.land/amazon-limits-product-titles-to-200-characters-starting-january-21/). **This limit is superseded by the 75-character rule, except for media.**
- Title style rules from the Seller Central help page "Product title requirements and guidelines":
  - These special characters are banned: ! $ ? _ { } ^ ¬ ¦. The exception is when they are part of the brand name.
  - ~ # < > * are allowed only in limited contexts, such as "Style #4301" or "<10 lb".
  - No word may appear more than twice. Prepositions, articles and conjunctions are exempt.
  - No promotional phrases, for example "100% quality guaranteed" or "free shipping".
  — [Seller Central help GYTR6SYGFA5E3EQC](https://sellercentral.amazon.com/gp/help/external/GYTR6SYGFA5E3EQC) (snippet only; full page not scraped)
- Vendor claim, unverified: singular and plural forms both count toward the two-use limit. — [search summary of myamazonguy / Goat Consulting](https://myamazonguy.com/news/2025-amazon-product-title-requirements/)
- Seller-reported issue: error **100476**, "This attribute 'Item Highlight' is currently unsupported", appeared even after titles were shortened below 75 characters. One AI-generated bullet was then flagged by Amazon's own moderation as "false/promotional claims". — [ppc.land, citing forum replies](https://ppc.land/amazon-cuts-product-title-limit-to-75-characters-on-july-27/)
  - Likely cause (inference from the SP-API rule above): Item Highlights is rejected until the stored `item_name` is 75 characters or fewer. A title edit that has not yet processed would trigger this.
- The forum thread drew more than 107 replies, mostly complaints about the short notice (about 47 days) and about industrial categories where specifications are defining. Dougal_Amazon pointed sellers to an "Engage With Amazon" Q&A. — [ppc.land](https://ppc.land/amazon-cuts-product-title-limit-to-75-characters-on-july-27/)

**Agency and vendor opinion**
- Liran Hirschkorn (Incrementum Digital) says:
  - Put brand, primary keyword, and "the one thing the buyer is actually searching" in the title.
  - Put secondary use cases, materials and comparison terms in Item Highlights.
  - Item Highlights are weighted more than backend search terms ("yes and yes").
  - Do not edit titles during peak events.
  — [ppc.land](https://ppc.land/amazon-cuts-product-title-limit-to-75-characters-on-july-27/)
- Jake McLaughlin says words in the title rank in order, with the first word carrying the most relevance. — [ppc.land](https://ppc.land/amazon-cuts-product-title-limit-to-75-characters-on-july-27/)
- keywords.am makes several claims:
  - Media (Books, Music, Video, DVD) keeps the 200-character limit.
  - The old category caps (150 for electronics, 125 for apparel, 80 for pet supplies) are gone.
  - Highlights "generally only show when the title is under 75 characters".
  - Title plus Item Highlights gives a combined searchable budget of about 200 characters.
  — [keywords.am, verified 4 Aug 2026](https://keywords.am/blog/amazon-character-limits/)
- SoldScope's own testing found that mobile search shows only about 30–40 characters of Item Highlights before truncating. Its advice: lead with material, pack count, certification or size; write short attribute phrases rather than sentences; keep child-specific values out of the parent title. — [SoldScope](https://www.soldscope.com/blog/amazon-item-highlights-desktop-august-10)

### Inferences
- For a leather goods seller, the 75-character title should hold brand, product type, and the main differentiator (for example "Full-Grain Leather").
- Item Highlights should hold secondary keywords such as fit or compatibility, use cases, and dimensions, front-loaded because truncation is about 30–40 characters on mobile.
- Write both fields yourself. Otherwise Amazon's AI rewrites apply, and without Brand Registry there is no 14-day review window.

### Gaps
- I could not read the official help page or the News_Amazon text in full. The exact wording on scope exceptions (beyond "media") and on CA/AU rollout timing is unconfirmed.
- Whether enforcement slipped from 27 July to 3 August is unconfirmed.
- No official Amazon statement on how word order or position is weighted. The claims above are practitioner opinion.

---

## 2. Bullet points

### Takeaway
Amazon's bullet requirements, effective 15 August 2024 and announced around 1 August 2024, cover the following:
- Prohibited special characters and emojis.
- Prohibited guarantee and refund claims.
- Amazon may use generative AI to improve bullets.
- A 10–255 character guideline per bullet.
- At least 3 bullets.

Third-party sellers get 5 bullets. A "first 1,000 bytes indexed" limit is widely repeated by vendors, but I found no Amazon source for it.

### Cited Findings
**Confirmed Amazon rules**
- Amazon's seller announcement says that effective 15 August 2024 it would update bullet point requirements: restricting special characters, emojis and certain phrases (for example refund guarantees), and using generative AI to help optimise listing quality. — [Seller Forums announcement (search snippet)](https://sellercentral.amazon.com/seller-forums/discussions/t/65f8e647-977d-49ac-9036-2049b96720b2); [tool4seller recap](https://www.tool4seller.com/blog/updated_bullet_point_requirements_0815.html)
- Conflict on review before publishing:
  - The bqool recap of Amazon's notice says AI improvements are shared "for review before Amazon publishes".
  - Goat Consulting says Amazon can edit or remove non-compliant bullets without approval.
  - Sellers in the forum asked where they could approve suggestions before publication.
  — [bqool](https://blog.bqool.com/ecommerce-news-roundup-august-recap-2024); [Goat Consulting](https://www.goatconsulting.com/amazon-policy/amazon-product-detail-page-rules-violation-policy-compliance)
- Vendor-listed prohibited characters: ™ ® € … † ‡ ¢ £ ¥ © ± ~ and all emojis. — [Goat Consulting (vendor)](https://www.goatconsulting.com/amazon-policy/amazon-product-detail-page-rules-violation-policy-compliance)

**Vendor opinion and secondary reporting**
- keywords.am describes three different limits:
  1. A guideline of 10–255 characters per bullet, at least 3 bullets, and no end punctuation, emojis, guarantees or pricing.
  2. A flat-file field that accepts up to 500 characters.
  3. Indexing of only the first 1,000 bytes across all bullets combined.
  It also says sellers get 5 bullets, and vendors (1P) can be eligible for up to 10 in some categories. — [keywords.am](https://keywords.am/blog/amazon-character-limits/)
- Other sources cite 256 or 500 characters, and say limits vary by category and flat-file template. — [search summary: wisepim, StoreAutomator, sellersasksellers](https://wisepim.com/guides/amazon-bullet-points)
- A Handmade forum thread notes that the help pages give 255 characters per bullet but no combined maximum. — [Seller Forums (EU)](https://sellercentral-europe.amazon.com/seller-forums/discussions/t/2135708b-0f8b-45dd-9795-6f14d1700830)

### Inferences
- Use 5 bullets of about 150–250 characters each.
- Start each bullet with a plain feature label, followed by a factual benefit with measurable specifications (dimensions, material grade, care). This structure suits both the compliance rules and AI or Rufus extraction.
- Avoid ™/®, emojis, "guarantee", "lifetime warranty" phrasing, and ending punctuation.

### Gaps
- No Amazon source for the 1,000-byte indexing limit. Treat it as vendor lore.
- No official Amazon guidance on "structure for AI extraction". Only vendor opinion exists.

---

## 3. Product description

### Takeaway
The description takes plain text up to 2,000 characters. HTML is no longer supported.

### Cited Findings
- 2,000-character cap, plain text. HTML support was removed in July 2021. Exceeding the cap returns an error and the listing will not save. For rich formatting, use A+ (Standard A+ allows up to 5 modules; Premium allows 7). — [keywords.am (vendor)](https://keywords.am/blog/amazon-character-limits/)

### Inferences
- Where A+ content is published it typically displays in place of the plain description. Still fill in the description, because it feeds data and search and appears where A+ is not shown. **This is a claim from my training knowledge; I did not verify it this session.**

### Gaps
- No primary Amazon source was retrieved on the 2,000-character limit, the removal of HTML, or whether descriptions are indexed when A+ exists.

---

## 4. Backend search terms and other hidden fields

### Takeaway
Generic keywords are limited to under 250 bytes (in practice 249) in the US and every other marketplace except India (200), Japan (500) and China. That should include CA and AU. Exceeding the limit suppresses indexing of the entire field. Use spaces, do not repeat words, and do not use brand names or ASINs.

### Cited Findings
- Amazon forum material from the 2017 rollout: "limits the length of the generic keywords attribute to less than 200 bytes in India, 500 bytes in Japan and 250 bytes in every other marketplace except China". Entries over the limit are suppressed or not indexed. Alphanumerics are 1 byte each; umlauts and similar are 2 bytes or more. — [Seller Forums, "Hidden Keywords"](https://sellercentral.amazon.com/seller-forums/discussions/t/cd2ba1dc90031ee378b37d4465a0e5ca)
  - This snippet says spaces and punctuation do not count.
  - keywords.am says spaces do count.
  - Treat 249 bytes including spaces as the safe working limit.
- Amazon staff and forum tips on search terms:
  - Spaces "work just fine" as separators.
  - Do not use brand names or ASINs.
  - Do not repeat words already in the title or bullets.
  - Include spelling variants but not misspellings, because Amazon's systems compensate for common misspellings.
  - The search system does not do partial matching.
  — [Seller Forums Quick Tip: Search Terms](https://sellercentral.amazon.com/seller-forums/discussions/t/0ae10d05-66d2-406b-b336-16791df2bce8); [AU version](https://sellercentral.amazon.com.au/seller-forums/discussions/t/c8d990af-c17d-4f49-8249-e863f7748e7e); [Generic Keyword format](https://sellercentral.amazon.com/seller-forums/discussions/t/1bc6e0da-5078-4438-ad07-31bcc7329484)
- Vendor claims:
  - Going over 249 bytes silently de-indexes all backend terms, with no error shown.
  - Some categories got a 500-byte expansion in 2024, but it was inconsistent, so 249 bytes remains the safe default.
  — [keywords.am](https://keywords.am/blog/amazon-character-limits/)
- Subject Matter, Intended Use and Target Audience: vendor guides from 2026 still describe them as active "free indexing" fields. Subject Matter is 5 lines of up to 50 characters. I found no Amazon deprecation notice. — [search summary: SellerSprite 2026 checklist](https://www.sellersprite.com/en/blog/Amazon-Backend-Search-Terms-The-2026-Complete-Checklist); [Helium 10](https://www.helium10.com/blog/use-amazon-search-terms-effectively/)

### Inferences
- CA (amazon.ca, including French terms, where accents cost 2 bytes) and AU should follow the 249-byte limit. Count bytes, not characters, for French-Canadian keywords.

### Gaps
- Official help page G23501 was not readable because of the rate limit.
- Whether Subject Matter, Intended Use and Target Audience are still indexed in 2026 is unconfirmed by Amazon. They appear only in some product-type templates.

---

## 5. Attributes, Listing Quality Dashboard, product type and browse nodes

### Takeaway
Attribute completeness clearly matters. However, the reports of a June 2026 "Attribute Completeness Score" in a revamped Listing Quality Dashboard come only from vendors, and the reports conflict on dates (9 June general availability versus late July). Product type governs restrictions and fees. Browse nodes govern browse and search placement. Wrong nodes are fixed through `recommended_browse_nodes` or `item_type_keyword`, or through a Seller Support or catalog case.

### Cited Findings
- Vendor-reported Listing Quality Dashboard changes:
  - novadata claims six components including an Attribute Completeness Score, with the full dashboard reaching general availability on 9 June 2026. Its figures come from its own 340-ASIN dataset.
  - Ecommerce Times or a similar outlet describes a consolidated Listing Quality Score rolling out in late July 2026.
  - These reports conflict, and neither is confirmed by Amazon.
  — [novadata](https://novadata.io/resources/news/amazon-listing-quality-dashboard-rollout-july-2026); [ecommerce-times](https://ecommerce-times.com/amazons-new-listing-quality-score-is-reshaping-fba-ranking-tactics/)
- Where to find it: Catalog > Manage All Inventory shows a per-SKU quality score, and Brands > Manage Your Brand > Listing Quality Dashboard has the detail. Brand Registry is needed for the per-attribute breakdown. — [Amalyze (vendor)](https://amalyze.com/resources/guides/listing/amazon-listing-quality-dashboard)
- Alternative navigation reported elsewhere: Inventory > Improve Listing Quality, which ranks missing attributes by priority. — [search summary: SellerCandy / PDMG](https://sellercandy.com/amazon-listing-quality-dashboard-explained)
- SellerSprite says the catalog has more than 750 data fields, and that the flat-file templates under "Add Products via Upload" list every attribute for a product type. Its claim that completeness outranks keyword density is opinion. — [SellerSprite](https://www.sellersprite.com/en/blog/amazon-agent-ready-attributes-audit-2026)
- Amazon moderator: "categories use the Product Type to determine what restrictions may be placed on selling products in that category as well as fees. Browse nodes are used for searching and browsing by buyers". The moderator pointed sellers to the Category-specific Browse Tree Guide (BTG). — [Seller Forums (EU)](https://sellercentral-europe.amazon.com/seller-forums/discussions/t/9becfa2e18ef5d986b5d6c239d768635)
- Workarounds reported by sellers:
  - Check Recommended Browse Nodes on the Vital Info tab.
  - Re-save the listing without changes.
  - Download a fresh template if the template was generated for the wrong product type.
  - Seller Support sometimes advises deleting and recreating the listing, which carries ASIN risk.
  — [Seller Forums error 8541](https://sellercentral-europe.amazon.com/seller-forums/discussions/t/46e2ac4f-b3e0-4d5f-b96d-49ffd625a9ce)
- Error 8011 means an invalid browse node. The fix is to use the deepest leaf node from the marketplace's own BTG; node IDs should not be reused across marketplaces. — [GoDataFeed (vendor)](https://www.godatafeed.com/disapproval/amazon-8011-invalid-browse-node)
- Amazon told sellers in 2023 that 274 attributes across 200 product types would become required for new listings. — [ChannelDock (vendor), search summary](https://channeldock.com/en/blogs/pim-data-quality-score-marketplaces/)

### Gaps
- No Amazon primary source for an "Attribute Completeness" launch in June 2026.
- No Amazon source for a "Fix Your Products" tool. It may be informal or vendor naming.
- No official 2026 procedure for product type or browse node reclassification was found beyond the forum workarounds above.

---

## 6. Variation families

### Takeaway
Variations must be the same product, differing only by an approved theme such as size, colour or pack. From 12 February to 31 May 2026, Amazon stopped sharing reviews across children with significant functional differences [AMAZON]. A new Add Products flow replaces the Variation Wizard, which retires by the end of August 2026. Merging different products, such as straps into a belt family, breaks the rules and now also splits reviews.

### Cited Findings
**Review-sharing change, announced on Seller Forums 7 January 2026**
- Reviews continue to be shared only for minor variations with the same function:
  - colour or pattern;
  - size with the same function (for example king versus queen bedding);
  - pack size or quantity;
  - secondary scent;
  - model fitment (for example phone cases for different phone models).
- Rollout by category from 12 February to 31 May 2026, with an email 30 days before a seller's products are affected.
- Amazon recommends reviewing variations in Manage All Inventory and using the correct theme (for example a colour theme for colour differences, not quantity).
- Reviews become eligible for sharing again if the theme is corrected afterwards.
— [ppc.land, 8 Jan 2026](https://ppc.land/amazon-splits-variation-reviews-in-bid-to-stop-misleading-ratings/) ([announcement](https://sellercentral.amazon.de/seller-forums/discussions/t/83ba401b-1295-44be-97b1-4ce263ab3c06))
- Conflict: some vendors treat pack quantity (for example a 2-pack versus a 10-pack) as functionally different. Amazon's list keeps pack size eligible. — [search summary: cahoot / jarvio](https://www.cahoot.ai/amazon-review-sharing-across-variations/)

**Earlier variation theme cleanup**
- On 26 August 2025, Amazon scaled back its variation theme cleanup after seller backlash. Existing families continue to work, and only themes with zero sales in the past 12 months are affected. — [ppc.land](https://ppc.land/amazon-halts-variation-theme-cleanup-after-seller-backlash/)

**New variation workflow, 21 July 2026**
- Products can be added to a family from Add Products > View Variations. Options are to add new variants, add existing standalone SKUs, or add an offer to existing variants. The flow uses a pre-filled spreadsheet with the family's attributes.
- It replaces the Variation Wizard, which retires by the end of August 2026.
- Family members must share brand and product type, with a matching theme on the parent and all children.
- Amazon warns that picking the wrong option can cause duplicates or an incorrect structure.
— [EcomCrew](https://www.ecomcrew.com/amazon-just-made-it-easier-to-add-variations-and-is-retiring-the-variation-wizard-in-august/); [Seller Forums](https://sellercentral.amazon.com/seller-forums/discussions/t/25e1f3ea-a691-4b01-baa4-db96d3ab7cb5)

**Rules against merging different products**
- Grouping unrelated products to borrow reviews or rank is a violation. Penalties include listing suppression, a policy warning, or the catalog team dismantling the family. — [Goat Consulting (vendor)](https://www.goatconsulting.com/merchandising/amazon-product-variations)

### Inferences
- A watch strap is a different product type from a belt, so it cannot sit in a belt family.
- To fix a family:
  - Break the family by blanking parent_sku and relationship_type on the child, or use a partial-update flat file with `update_delete`.
  - Re-parent through the new Add Products variation flow.
- For discontinued children, set quantity to 0 and close the offer or delete the child SKU. **These mechanics are from my training knowledge; I did not verify them this session.**

### Gaps
- No official 2026 help text was retrieved on breaking or re-parenting variations, or on cleaning up discontinued children.

---

## 7. Restricted claims and the Product Detail Page Rules

### Takeaway
Detail page text must not contain promotional or boastful claims ("top-rated", "#1", "best-selling"), guarantees or refund promises, unsubstantiated environmental claims ("eco-friendly"), or another brand's name except in the prescribed "compatible with" format.

### Cited Findings
- Environmental claims: Amazon's Environmental Marketing Guidelines require compliance with the FTC Green Guides and applicable state and local law. — [Seller Central G201893650](https://sellercentral.amazon.com/help/hub/reference/external/G201893650)
- EU only: a vendor reports that Amazon is deactivating environmental claims that do not comply with the EU ECGT Directive after 27 September 2026, unless substantiation is uploaded. — [AMALYTIX (vendor)](https://www.amalytix.com/en/blog/ecgt-amazon-listings/)
- Consultants list "100% satisfaction guaranteed", "top-rated", "#1 rated" and "best-selling" as not allowed. Guarantee or warranty claims, and references to off-Amazon refund policies, are also not allowed, in A+ as well. — [myamazonguy](https://myamazonguy.com/prohibited-keywords/); [ecomclips](https://ecomclips.com/blog/restricted-words-in-amazon-a-and-how-can-we-use-them-to-avoid-restriction/)
- Other brands' names: Amazon's IP policy allows a third-party brand name only to state true compatibility, in this format: [Your brand] [product] "compatible with" / "fits" / "intended for" [Other brand] [product]. Logos are not allowed. Titles in any other format may be removed as potentially infringing. — [Seller Forums thread](https://sellercentral.amazon.com/seller-forums/discussions/t/e4c041c3fa577b6a3f5ebd9352c8487c); [EcommerceBytes 2020 (archived)](https://www.ecommercebytes.com/2020/11/11/new-amazon-guidance-on-brand-compatibility/)
- Competitor brands are also prohibited in backend search terms. — [Seller Forums Quick Tip](https://sellercentral.amazon.com/seller-forums/discussions/t/0ae10d05-66d2-406b-b336-16791df2bce8)

### Inferences
- An "Apple" mouse pad title is only acceptable if the product truly is a fit for an Apple product, and then only in "compatible with Apple MacBook" form. Even then it risks IP complaints.
- Unverified certification claims (for example "LWG certified") should be removed unless substantiated. Use the relevant structured certification attributes.

### Gaps
- The full Product Detail Page Rules (G200390640) and Amazon's restricted-claims text could not be retrieved this session.
