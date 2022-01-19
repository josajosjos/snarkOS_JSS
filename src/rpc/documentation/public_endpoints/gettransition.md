# Get Transition 
Returns a transition given the transition ID.

### Arguments

|    Parameter    |  Type  | Required |                    Description                     |
|:---------------:|:------:|:--------:|:--------------------------------------------------:|
| `transition_id` | string |   Yes    | The transition id of the requested transition info |

### Response

|    Parameter     |  Type  |                                  Description                                  |
|:----------------:|:------:|:-----------------------------------------------------------------------------:|
|  `ciphertexts`   | array  |                    The ciphertexts of the output records.                     |
|  `commitments`   | array  |                    The commitments of the output records.                     |
|     `events`     | array  |                    The events emitted from the transition.                    |
|     `proof`      | string |    The zero-knowledge proof attesting to the validity of this transition.     |
| `serial_numbers` | array  |                   The serial numbers of the input records.                    |
| `transition_id`  | string |                          The ID of this transition.                           |
| `value_balance`  | number | A value balance is the difference between the input and output record values. |


### Example Request
```ignore
curl --data-binary '{"jsonrpc": "2.0", "id":"1", "method": "gettransition", "params": ["as1xuppwj4x7eswxppdlg3pt49vue2kwfw3cw8m8k3uqxe5e7945g9s4s8lz5"] }' -H 'content-type: application/json' http://127.0.0.1:3030/
```

### Example Response
```json
{
  "jsonrpc": "2.0",
  "result": {
    "ciphertexts": [
      "recd1v76mftwzagt9k9nsjjpdqgytv4ddk24e9q7f240daar7avcv3q9gd9rx6c230n99jhxfj24xpvkrr5vk04fl2kapa0a0a895hvevzq7tnwuat9lzwpy4c4rxys6uaj34098295t9fff7khqctvkcglumqlvg47rwzhqhw9u5zxfhug9dde67dyjc6uflp4x028mrmzkhfa6qn0l6jju8lfhmy5crcqqefjv8m4zwv34tvk03d65gdmv4fe35wtgy6rmy4heq89uwh0hqe40k2g7nyj2rk6xlgqnf724pt6ynkefxwypmvhhjzk806re4njej552jfq74ej0ykhrcxa93l9n6rkchlhuuzz2fpqtt2npqz8avnv442ng4djm8lve4dlqfelpjjn5yj425rs98pvn5k54gvn5vku3wek3ytxe8zpen7n2saf060j97u8yyygt4y9zqklnek3v",
      "recd1u5chlqz8n80rwem25de9npujv2uh006yajgyum9p5kn4rsu9s5ymgrwgle39pz87s0726g4rg47dx5nl330680gxmyxffyg7p77qvppfql3p3hxncp9fpus8upsa5nlfwfnck7k4hzcjskrnrfza6tqcpgvquuv663ahswju6s3wcawh9ktz87ewzgpj2nc8gc9wd30zc8zsgu5xyen4q352u7y6l985kv2hq6nx9hu4n4mhgglacw7dc026y6qglwh0l302gwxs0s804waax472h4tv2npmprtvp5hkzg7hhm360squhgnxtpdthh0ncyrdklqy57nlfr6z5dm080xd2z9uw3h9fpu9vqsy9q4vakw00wk0prwf92ekmnh9e00v4l2a4sldmcnzcj90p75nqlrd5ek80e6l3xz559meskjeq7kpyhftsxcptc9d009xuh6nxlyszq7uktv"
    ],
    "commitments": [
      "cm1xck4eyf3a3qnz69yyrr3jf698mqzwpjgkqu0j359p0sdr5wyjyqsn0604p",
      "cm1up0j5cq0k3w96skhsq750m6alw8dcau5msn390h8fpkgny5zdvps9h9dp8"
    ],
    "events": [
      {
        "id": 1,
        "index": 0,
        "record_view_key": "rcvk1mujt98tc2r04l58haxjv48s5a7vnhx8ws24fxpdruuk3z37vscqsjtvlg5"
      },
      {
        "id": 1,
        "index": 1,
        "record_view_key": "rcvk1yuqvyczasq876gjt8xwz7d2dxzs3umlp8nccpcg3nmlp4qxs35yqgflhy6"
      }
    ],
    "proof": "ozkp1fhewv363wgl04jcxdnmaznkeszy2svj6ncxr9pl5f5l3lm6mgsr8e6tqxpkhhtxc6pesfd40hxfgwz7luqwwa00uwzu5s8jfq9n743n4y4dldf9htr20jv9zpw59cf4xxwurnpckq0wt8r5hfdn5m2d9qryk20yz9zfeyvv7hrexxvd707qx730q2qeppnu70y0q3rpnqzprtxrclgqptrwlx2cdzg5ywkayn8f04xelpge4d73a3tmyvlyuj5phlv5lxq2afh4zaxnxw8f2e5k32xu9w0vmq7xldqmyv7pxjfj2mzqrwyagg7nzsay34kx2zutx33r0eugfqgtqlhrzrnhqu2npk0kxwcx27rgvpfcwemsns56d7xn0zety5mkcje3ud0usjfhmdwhh3eypzh0x3svs5jhm9nhtpqc7j7ms3gu4rc7d352g42fzv2vvv5lsxuygzqgxrha3j",
    "serial_numbers": [
      "sn1m70m3egkxqq5dmalym3hf5arz296k37h87kv4ztge48c3a6hmcysw22avz",
      "sn1q8y49taxgquprav54nkd42n8dd8egj0rghjfg834q0zlfv3p9cpst9mkj5"
    ],
    "transition_id": "as1xuppwj4x7eswxppdlg3pt49vue2kwfw3cw8m8k3uqxe5e7945g9s4s8lz5",
    "value_balance": -1000000000000000
  },
  "id": "1"
}
```