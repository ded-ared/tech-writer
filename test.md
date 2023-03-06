# Bank Card Details

<table class="table" style="table-layout: fixed;" cellpadding="0" cellspacing="0">
	<tr valign="top" align="center">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif"><b>Field</b></font></p>
		</td>
		<td width="70%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>Description</b></font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>Type</b></font></p>
		</td>
		<td width="70%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif"><b>Bank card</b> as a payment method is selected from the drop-down list.</font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>Subtype</b></font></p>
		</td>
		<td width="70%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Payment method configured in the <b>Integrations → Payment methods</b> section of the Dashboard and selected from the drop-down list.</font></p>
		</td>
	</tr>
	<tr valign="top" align="center">
		<td colspan="2" width="100%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif">The fields below are available for both <b>Data</b> and <b>Fixed data</b> sections.</font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>First name</b></font></p>
		</td>
		<td width="70%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">First name of the card holder as written on the bank card. The field may contain a <b>Cardholder</b> title (or something like that) if the card is non-personalized.</font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>Last name</b></font></p>
		</td>
		<td width="70%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Last name of the card holder as written on the bank card.<br><br>The field may be blank if the card is non-personalized.</font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>Number</b></font></p>
		</td>
		<td width="70%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Card number.<br><br>Only the first four and last four digits are shown.</font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>Valid until</b></font></p>
		</td>
		<td width="70%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Card expiry date in the <code>YYYY-MM</code> format.</font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>Issue date</b></font></p>
		</td>
		<td width="70%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Card issue date if there is such information on the card.</font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>Transaction amount</b></font></p>
		</td>
		<td width="70%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">The amount of the current transaction.<br><br>The field may be blank if the applicant is uploading the card data only for registering and not for a particular transaction.</font></p>
		</td>
	</tr>
</table>

⚠️ Fixed data is the card info that you can submit to us via API to compare with extracted data.


# Crypto-wallet Details

<table class="table" style="table-layout: fixed;" cellpadding="0" cellspacing="0">
	<tr valign="top" align="center">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif"><b>Field</b></font></p>
		</td>
		<td width="70%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>Description</b></font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>Type</b></font></p>
		</td>
		<td width="70%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif"><b>Crypto-wallet</b> as a payment method is selected from the drop-down list.</font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>Subtype</b></font></p>
		</td>
		<td width="70%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Payment method configured in the <b>Integrations → Payment methods</b> section of the Dashboard and selected from the drop-down list.</font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>ERC-20 Token</b></font></p>
		</td>
		<td width="70%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">For detailed info, refer to <a href="https://developers.sumsub.com/applicant-actions/tokenList.html">ERC-20 Token ID</a></font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>Payment direction</b></font></p>
		</td>
		<td width="70%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Available options:<br>
			<ul>
				<li><b>Deposit</b> — that is put in the applicant’s account</li>
				<li><b>Withdrawal</b> — that is taken out of the applicant’s account</li>
			</ul></font></p>
		</td>
	</tr>
	<tr valign="top" align="center">
		<td colspan="2" width="100%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif">The fields below are available for both <b>Data</b> and <b>Fixed data</b> sections.</font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>Wallet address/Fixed Wallet address</b></font></p>
		</td>
		<td width="70%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Applicant wallet address.</font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>Transaction</b></font></p>
		</td>
		<td width="70%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Crypto transaction hash.</font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>Issue date</b></font></p>
		</td>
		<td width="70%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Issue date is ignored in case of crypto check so this field stays blank.</font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>Transaction amount</b></font></p>
		</td>
		<td width="70%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Transaction amount if applicable to the document.<br><br>The field may be blank if the applicant is uploading the wallet data only for registering and not for a particular transaction.</font></p>
		</td>
	</tr>
</table>

⚠️ Fixed data is the crypto-wallet and transaction info that you can submit to us via API to compare with extracted data.






```mermaid
graph TB
A((Inception</br>I wonder how long</br>the text can be here)) ---> B(Vers 1)
A --> C{Vers 2}
A ---> D(Vers 3)
C --> E(Vers Next 1)
C --> F(Vers Next 2)
C --> G(Vers Next 3)

```






# Table

<table class="table" style="table-layout: fixed;" cellpadding="0" cellspacing="0">
	<tr valign="top">
		<td width="30%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif"><b>Колонка
			1 Строка 1</b></font></p>
		</td>
		<td colspan="2" width="70" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif"><b>Колонка 2-3</b></font></p>
		</td>
	</tr>
	<tr valign="top">
		<td rowspan="4" width="30%" style="border: 1px solid #000000; padding: 0cm"><p>
			<font face="Arial, sans-serif">Колонка 1 Строка 2-4</font></p>
		</td>
		<td width="35%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Колонка
			2 Строка 2</font></p>
		</td>
		<td width="35%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Колонка
			3 Строка 2</font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="35%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Колонка
			2 Строка 3</font></p>
		</td>
		<td width="35%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Колонка
			3 Строка 3</font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="35%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Колонка
			2 Строка 4</font></p>
		</td>
		<td width="35%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Колонка
			3 Строка 4</font></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="35%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Колонка
			2 Строка 5</font></p>
		</td>
		<td width="35%" style="border: 1px solid #000000; padding: 0cm"><p><font face="Arial, sans-serif">Колонка
			3 Строка 5</font></p>
		</td>
	</tr>
</table>

# GRAPH

```mermaid
graph LR
A[Square Rect] -- Link text --> B((Circle))
A --> C(Round Rect)
B --> D{Rhombus}
C --> D
```

# TABLES

# 

| Left-Aligned  | Center Aligned  | Right Aligned |
|:------------- |:---------------:| -------------:|
| col 3 is      | some wordy text |     **$1600** |
| col 2 is      | centered        |         $12   |
| zebra stripes | are neat        |        ~~$1~~ |

<table _ngcontent-jsn-c151="" class="table" style="table-layout: fixed;" width="100%" contenteditable="false">
    <thead>
        <th colspan="3" align="left">Text for columns: 1 and 2 (Merged)</th>
    </thead>
    <tr>
        <td><b>Column 1. Row 2 Text</b></td>
        <td colspan="2"><b>Column 2. Row 2 Text</b></td>
    </tr>
    <tr>
        <td>Column 1. Row 3 Text</td>
        <td>Column 2. Row 3 Text</td>
        <td>Column 3. Row 3 Text</td>
    </tr>
</table>

Information!
For your convenience, there is a placeholder in each field to get the idea of how it should be filled in.

Settings Table

<table _ngcontent-jsn-c151="" class="table" style="table-layout: fixed;" contenteditable="false">
   <thead>
      <tr>
         <th>Column 1</th>
         <th>Column 2</th>
         <th>Column 3</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td colspan="2" style="text-align: center; vertical-align: middle;">Text for columns: 1 and 2 (Merged)</td>
         <td>Text for column 3</td>
      </tr>
      <tr>
         <td>Text for column 1</td>
         <td>Text for column 2</td>
         <td>Text for column 3</td>
      </tr>
      <tr>
        <td rowspan="3" style="vertical-align: middle;">Text for rows 1 to 3 (Merged)</td>
        <td>Text for column 2</td>
        <td>Text for column 3</td>
      </tr>
      <tr>
        <td>Text for column 2</td>
        <td>Text for column 3</td>
      </tr>
      <tr>
        <td>Text for column 2</td>
        <td>Text for column 3</td>
      </tr>
      <tr>
        <td>Text for column 1</td>
        <td td colspan="2" style="text-align: center; vertical-align: middle;">Text for columns: 2 and 3</td>
     </tr>
     <tr>
        <td>Text for column 1</td>
        <td>Text for column 2</td>
        <td>Text for column 3</td>
     </tr>
     <tr>
        <td>Text for column 1</td>
        <td rowspan="3" style="vertical-align: middle;">Text for column 2 (Merged 3 rows of the second column).</td>
        <td>Text for column 3</td>
     </tr>
     <tr>
        <td>Text for column 1</td>
        <td>Text for column 3</td>
      </tr>
      <tr>
        <td>Text for column 1</td>
        <td>Text for column 3</td>
      </tr>
   </tbody>
</table>
