from requests import get, post
server_url = 'https://mobile-phone-server.vercel.app/phones'
res = get(server_url)
if res.status_code == 200:
    data = res.json()
    phones = data.get('RECORDS')
def media_from_urL(img_src, phone_alt):
    codes = f'< !-- wp: image {{"align": "center", "sizeSlug": "large"}} -->'\
    f'< figure class ="wp-block-image aligncenter size-large" >'\
    f'<img src="{img_src}" alt="{phone_alt} image" / >' \
    f'< figcaption class ="wp-element-caption" > {phone_alt} < / figcaption > < / figure >'\
    f'< !-- / wp: image -->'

    return codes

    test = media_from_url ('https://www.gsmarena.com.bd/images/products/Oppo-K11x.jpg')

    print(test)


def wp_table_dict(dictionary):

   codes = '< !-- wp: table --> < figure class ="wp-block-table" > < table > < tbody >'
   for key, value  in dictionary.items():
       tr_data = f'< tr >< td >{key} < /td >< td > {value}< /td >< /tr >'

   codes+= '< /tbody >< /table >< /figure >< !-- / wp: table -->'

   return codes




