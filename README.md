<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Local NJ Curated Shop | Cash &amp; Shipping</title>
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; }
        body { background-color: #f4f6f8; color: #333; padding: 20px; }
        header { text-align: center; padding: 40px 20px; background-color: #ffffff; border-bottom: 1px solid #eaeaea; margin-bottom: 30px; border-radius: 8px; box-shadow: 0 2px 4px rgba(0,0,0,0.02); }
        header h1 { font-size: 26px; margin-bottom: 10px; color: #111; }
        header p { color: #666; font-size: 15px; max-width: 600px; margin: 0 auto; line-height: 1.4; }
        .container { max-width: 900px; margin: 0 auto; display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; }
        .product-card { background: #ffffff; border: 1px solid #eaeaea; border-radius: 8px; overflow: hidden; display: flex; flex-direction: column; box-shadow: 0 4px 6px rgba(0,0,0,0.02); }
        .product-image { width: 100%; height: 320px; background-color: #eee; object-fit: cover; display: block; }
        .product-info { padding: 25px; flex-grow: 1; display: flex; flex-direction: column; }
        .product-title { font-size: 18px; font-weight: 600; margin-bottom: 8px; color: #111; }
        .product-price { font-size: 22px; font-weight: 700; color: #2e7d32; margin-bottom: 12px; }
        .product-desc { font-size: 14px; color: #555; line-height: 1.6; margin-bottom: 20px; white-space: pre-line; }
        
        /* Form & Status Styles */
        .reserve-form { border-top: 1px solid #eee; padding-top: 20px; margin-top: auto; }
        .reserve-form label { display: block; font-size: 12px; font-weight: 600; text-transform: uppercase; color: #777; margin-bottom: 5px; }
        .reserve-form input, .reserve-form select { width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 4px; margin-bottom: 12px; font-size: 14px; background-color: #fff; }
        .reserve-button { width: 100%; background-color: #2e7d32; color: white; border: none; padding: 12px; font-size: 15px; font-weight: 600; border-radius: 5px; cursor: pointer; transition: background-color 0.2s; }
        .reserve-button:hover { background-color: #1b5e20; }
        .reserve-button:disabled { background-color: #999; cursor: not-allowed; }
        
        /* Custom Ajax Success Message Container */
        #success-message { display: none; background: #e8f5e9; border: 1px solid #c8e6c9; border-radius: 6px; padding: 20px; margin-top: 15px; text-align: center; }
        #success-message h3 { color: #2e7d32; margin-bottom: 10px; }
        #success-message p { font-size: 14px; color: #2e7d32; line-height: 1.4; }
        .zone-badge { background: #ffffff; border: 1px dashed #2e7d32; padding: 10px; margin-top: 10px; font-weight: bold; border-radius: 4px; color: #1b5e20; text-align: left; font-size: 13px; line-height: 1.5; }
        .error-msg { color: #d32f2f; font-size: 12px; margin-top: 5px; display: block; }
    </style>
</head>
<body>

    <header>
        <h1>Local NJ Curated Collection</h1>
        <p>Browse available clothing and inheritance pieces online. Reserve your item below for secure nationwide shipping or cash pickup at a safe local venue.</p>
    </header>

    <div class="container">
        <!-- PRODUCT ITEM CARD -->
        <div class="product-card">
            <!-- Your Verified Postimages AVIF link is locked into the line below -->
            <img class="product-image" src="https://postimg.cc" alt="Handmade 19th C Russian Blue Trade Beads">
            <div class="product-info">
                <div class="product-title">Handmade 19th C. Russian Blue Periwinkle Glass Trade Beads</div>
                <div class="product-price">$484.00</div>
                <div class="product-desc"><strong>Ultra-rare antique 19th-century "Russian Blue" faceted glass trade beads.</strong> This listing features a highly prized museum-quality collection of three full strands, exceptionally rare due to being completely intact on their original 1800s natural raffia fiber stringing. Masterfully hand-faceted by Bohemian glass artisans and distributed along historic trade routes, these highly sought-after collector pieces showcase an incredible semi-translucent periwinkle blue hue.

<strong>Price for the full 3-strand collection: $484</strong> (Total 440 beads — bundle discount applied!)

<em>Exact bead counts and individual pricing per strand:</em>
• Strand 1: 144 beads – $165
• Strand 2: 146 beads – $170
• Strand 3: 150 beads – $180

"Blue sky caught in glass, traveling the rivers to buy a fortune in furs."

Authentic age patina, irregular hand-cut facets, and immense historical significance make this bundle a true rarity for serious historians, antique bead collectors, and premium jewelry designers. Please use the form below to choose your fulfillment preference (Local Pickup or Secure Mail Shipping).</div>
                
                <!-- Live Ajax Formspree Connection -->
                <form id="nj-reserve-form">
                    <input type="hidden" name="Item_To_Buy" value="Russian Blue Trade Beads Collection - $484">
                    
                    <label for="name">Your Name</label>
                    <input type="text" id="name" name="Buyer_Name" required placeholder="e.g., Jane Doe" data-fs-field>
                    
                    <label for="email">Email Address</label>
                    <input type="email" id="email" name="Buyer_Email" required placeholder="e.g., jane@email.com" data-fs-field>
                    <span data-fs-error="email" class="error-msg"></span>
                    
                    <label for="delivery-preference">How would you like to receive this item?</label>
                    <select id="delivery-preference" name="Fulfillment_Method" required>
                        <option value="" disabled selected>Select fulfillment option...</option>
                        <option value="Secure Mail Shipping (Paid Upfront)">Secure Mail Shipping (Paid Upfront)</option>
                        <option value="Local Cash Pickup (Bank, Library, or Police Station)">Local Cash Pickup (Bank, Library, or Police Station)</option>
                    </select>

                    <label for="location-note">Your Shipping Address OR Preferred Local Meetup City</label>
                    <input type="text" id="location-note" name="Buyer_Location_Details" required placeholder="Type full shipping address OR local meetup city...">
                    
                    <button type="submit" class="reserve-button" data-fs-submit-btn>Submit Order Request</button>
                </form>

                <!-- On-Page Success Announcement Container -->
                <div id="success-message" data-fs-success>
                    <h3>🎉 Order Request Received!</h3>
                    <p>Your request is safe. We have logged your delivery preference and placed this 3-strand collection on temporary hold.</p>
                    <div class="zone-badge">
                        • <strong>If Shipping was selected</strong>: We will calculate exact postage, handling, and parcel insurance, then email you a secure digital payment link to pay upfront.<br>
                        • <strong>If Local Pickup was selected</strong>: We will email you to finalize a secure cash-only transaction at a nearby bank, library, or police station.
                    </div>
                    <p style="margin-top: 10px; font-size: 13px; color: #555;">Check your inbox shortly! We will reach out to you within 2 hours to finalize the next steps.</p>
                </div>
                <div data-fs-error class="error-msg" style="text-align:center; margin-top:10px;"></div>
            </div>
        </div>
    </div>

    <footer>
        <p>&copy; 2026 Local NJ Marketplace. Secure Independent Sales.</p>
    </footer>

    <!-- Formspree Ajax SDK Scripts -->
    <script>
      window.formspree = window.formspree || function () { (formspree.q = formspree.q || []).push(arguments); };
      formspree('initForm', { formElement: '#nj-reserve-form', formId: 'mbgrjjko' });
    </script>
    <script src="https://unpkg.com" defer></script>
</body>
</html>

