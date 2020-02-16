# CV

1. My name is  __Aliaksandr Prakapenka__. I'm 28 years old.
2. Contacts:
    - Mobile phone - +375 29 960 90 32 _(A1)_
    - Telegram - @alex27prok
3. I want to improve my skills in programming languages. The main goal is connecting my life with software developing. I know, that a lot of developers use programming languages and technologies for web and, as result, I've made a choise to learn JS.
4. I'm a head of IT-department of Minsk State Linguistik University. I've been working there for about 7 years. I have a lot of knowledge about different software products and systems what is used in the university. I use some programming languages: PHP _(Yii2)_, C++ _(Qt)_, C# for creating small projects for the university.
5. Code example:
```sh
public function actionLocality() {
        $out = [];
        if (isset($_POST['depdrop_parents'])) 
        {
            $ids = $_POST['depdrop_parents'];
            //print_r($ids);
            $area = $ids[0];
            $region = $ids[1];
            $type = $ids[2];
            if ($type != null) {
                $list = Locality::find()->select(['id_locality','name_locality'])->where(['area' => $area,'region'=>$region,'type_locality'=>$type])->asArray()->all();
                $selected  = null;
                if (count($list) > 0)
                {
                    foreach ($list as $i => $locality) {
                        $out[] = ['id' => $locality['id_locality'], 'name' => $locality['name_locality']];
                    }
                    // Shows how you can preselect a value
                    echo Json::encode(['output' => $out, 'selected'=>'']);
                    return;
                }
            }
        }
        echo Json::encode(['output'=>'', 'selected'=>'']);
    }
```
