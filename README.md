# React-Phone-Input With Accessibility
 ## react-phone-input-with-accessibility
A React component for phone number input with built-in accessibility support.

![animation](https://media.giphy.com/media/xiORAWnqoTJDsH0UOI/giphy.gif)

## Installation
```shell-script
npm install react-phone-input-with-accessibility
```

```shell-script
yarn add react-phone-input-with-accessibility
```

## Usage
```jsx
import PhoneInput from 'react-phone-input-with-accessibility'
import 'react-phone-input-with-accessibility/lib/style.css'

<PhoneInput
  country={'us'}
  value={this.state.phone}
  onChange={phone => this.setState({ phone })}
/>
```
**available styles** - style • high-res • material • bootstrap • semantic-ui • plain

## Options
<table>
  <tr>
    <th> Name </th>
    <th> Type </th>
    <th> Description </th>
    <th> Example </th>
  </tr>
  <tr>
    <td> country </td>
    <td> string </td>
    <td> initial country </td>
    <td> 'us' | 1 </td>
  </tr>
  <tr>
    <td> value </td>
    <td> string </td>
    <td colspan="2"> input state value </td>
  </tr>

  <tr>
    <td> onlyCountries </td>
    <td> array </td>
    <td> country codes to be included </td>
    <td> ['cu','cw','kz'] </td>
  </tr>
  <tr>
    <td> preferredCountries </td>
    <td> array </td>
    <td> country codes to be at the top </td>
    <td> ['cu','cw','kz'] </td>
  </tr>
  <tr>
    <td> excludeCountries </td>
    <td> array </td>
    <td> array of country codes to be excluded </td>
    <td> ['cu','cw','kz'] </td>
  </tr>

  <tr>
    <td> placeholder </td>
    <td> string </td>
    <td colspan="2"> custom placeholder </td>
  </tr>

  <tr>
    <td> inputProps </td>
    <td> object </td>
    <td colspan="2"> props to pass into the input </td>
  </tr>
</table>

<table>
  <tr>
    <th> Booleans </th>
    <th> Default </th>
    <th> Description </th>
  </tr>
  <tr>
    <td> autoFormat </td>
    <td> true </td>
    <td> on/off phone formatting </td>
  </tr>
  <tr>
    <td> disabled </td>
    <td> false </td>
    <td> disable input and dropdown </td>
  </tr>
  <tr>
    <td> disableDropdown </td>
    <td> false </td>
    <td> disable dropdown only </td>
  </tr>
  <tr>
    <td> disableCountryCode </td>
    <td> false </td>
    <td> </td>
  </tr>
  <tr>
    <td> enableAreaCodes </td>
    <td> false </td>
    <td> enable local codes for all countries </td>
  </tr>
  <tr>
    <td> enableTerritories </td>
    <td> false </td>
    <td> enable dependent territories with population of ~100,000 or lower </td>
  </tr>
  <tr>
    <td> enableLongNumbers </td>
    <td> false </td>
    <td> boolean/number </td>
  </tr>
  <tr>
    <td> countryCodeEditable </td>
    <td> true </td>
    <td> </td>
  </tr>
  <tr>
    <td> enableSearch </td>
    <td> false </td>
    <td> enable search in the dropdown </td>
  </tr>
  <tr>
    <td> disableSearchIcon </td>
    <td> false </td>
    <td> hide icon for the search field </td>
  </tr>
</table>

```jsx
<PhoneInput
  inputProps={{
    name: 'phone',
    required: true,
    autoFocus: true
  }}
/>
```

### Contents
- [Style](#style)
- [Events](#events)
- [Regions](#regions)
- [Localization](#predefined-localization)
- [Local area codes](#local-area-codes)
- [Custom masks](#custom-masks)
- [Custom area codes](#custom-area-codes)

### Style
<table>
  <tr>
    <td> containerClass </td>
    <td> string </td>
    <td colspan="2"> class for container </td>
  </tr>
  <tr>
    <td> inputClass </td>
    <td> string </td>
    <td colspan="2"> class for input </td>
  </tr>
  <tr>
    <td> buttonClass </td>
    <td> string </td>
    <td colspan="2"> class for dropdown button </td>
  </tr>
  <tr>
    <td> dropdownClass </td>
    <td> string </td>
    <td colspan="2"> class for dropdown container </td>
  </tr>
  <tr>
    <td> searchClass </td>
    <td> string </td>
    <td colspan="2"> class for search field </td>
  </tr>

  <tr>
    <td> containerStyle </td>
    <td> object </td>
    <td colspan="2"> styles for container </td>
  </tr>
  <tr>
    <td> inputStyle </td>
    <td> object </td>
    <td colspan="2"> styles for input </td>
  </tr>
  <tr>
    <td> buttonStyle </td>
    <td> object </td>
    <td colspan="2"> styles for dropdown button </td>
  </tr>
  <tr>
    <td> dropdownStyle </td>
    <td> object </td>
    <td colspan="2"> styles for dropdown container </td>
  </tr>
  <tr>
    <td> searchStyle </td>
    <td> object </td>
    <td colspan="2"> styles for search field </td>
  </tr>
</table>

### Events
<table>
  <tr>
    <td> onChange </td>
    <td> onFocus </td>
    <td> onBlur </td>
    <td> onClick </td>
    <td> onKeyDown </td>
  </tr>
</table>

onChange(value, country, e, formattedValue)

Country data object not returns from onKeyDown event

<table>
  <tr>
    <th> Data </th>
    <th> Type </th>
    <th> Description </th>
  </tr>
  <tr>
    <td> value/event </td>
    <td> string/object </td>
    <td> event or the phone number </td>
  </tr>
  <tr>
    <td> country data </td>
    <td> object </td>
    <td> country object { name, dialCode, countryCode (iso2) } </td>
  </tr>
</table>

### Regions
<table>
  <tr>
    <th> Name </th>
    <th> Type </th>
    <th> Description </th>
  </tr>
  <tr>
    <td> regions </td>
    <td> array/string </td>
    <td> to show countries only from specified regions </td>
  </tr>
</table>

<table>
  <tr>
    <th> Regions </th>
  </tr>
  <tr>
    <td> ['america', 'europe', 'asia', 'oceania', 'africa'] </td>
  </tr>
  <tr>
    <th> Subregions </th>
  </tr>
  <tr>
    <td> ['north-america', 'south-america', 'central-america', 'carribean', 'eu-union', 'ex-ussr', 'ex-yugos', 'baltic', 'middle-east', 'north-africa'] </td>
  </tr>
</table>

```jsx
<PhoneInput
  country='de'
  regions={'europe'}
/>

<PhoneInput
  country='us'
  regions={['north-america', 'carribean']}
/>
```

### Predefined localization
`es` Spanish, `de` Deutsch, `ru` Russian, `fr` French<br/>
`jp` Japanese, `cn` Chinese, `pt` Portuguese, `it` Italian<br/>
`ir` Iranian, `ar` Arabic, `tr` Turkish, `id` Indonesian<br/>
`hu` Hungarian, `pl` Polish, `ko` Korean

```jsx
import es from 'react-phone-input-with-accessibility/lang/es.json'

<PhoneInput
  localization={es}
/>
```

### Local area codes
```jsx
<PhoneInput
  enableAreaCodes={true}
  enableAreaCodes={['us', 'ca']}
  enableAreaCodeStretch
/>
```

#### Flexible mask
If `enableAreaCodeStretch` is added, the part of the mask with the area code will not stretch to length of the respective section of phone mask.
Example: `+61 (2), +61 (02)`

### Custom masks
```jsx
<PhoneInput
  onlyCountries={['fr', 'at']}
  masks={{fr: '(...) ..-..-..', at: '(....) ...-....'}}
/>
```

### Custom area codes
```jsx
<PhoneInput
  onlyCountries={['gr', 'fr', 'us']}
  areaCodes={{gr: ['2694', '2647'], fr: ['369', '463'], us: ['300']}}
/>
```

### Accessibility Support

This component is built with accessibility in mind and can be easily navigated using the keyboard or assistive technologies. It includes proper ARIA attributes and keyboard interaction for a seamless experience for all users.


Make sure you donated for lib maintenance [!Donate](https://www.paypal.com/donate/?hosted_button_id=E9HMRALLDVVHQ)
