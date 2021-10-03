## Creating Articles

In order to create an assignment/article object in the database, you can make a POST request to `/api/v1/article` with the sample JSON below. It will create an assignment with the followings,
- Sample article text
- Section with multiple choice questions
- Section with ordering questions
- Section with true/false questions
- Section with matching questions
- Section with fill-in-the-blank questions

----

```yaml
{
    "text": {
        "title": "Assignment1",
        "text": "Aliquam in leo massa. Pellentesque egestas risus vitae nunc ultricies, non posuere ex mattis. Duis lorem eros, viverra ac laoreet ac, tincidunt in dolor. Donec viverra ullamcorper neque at placerat. Etiam consequat dignissim justo, ac lobortis diam pretium sed. Suspendisse sagittis nec sem eget convallis. Integer non purus sem. Sed mi sapien, molestie in scelerisque in, luctus a libero. Integer pharetra, tellus et iaculis convallis, nunc dui bibendum diam, vel porttitor augue tortor eu felis. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Etiam rutrum, risus a tempor pulvinar, magna dui dapibus justo, vitae condimentum dui urna vitae ipsum. Donec placerat ante euismod, hendrerit ex et, dictum ligula. Proin eu tellus in lorem vestibulum dignissim in nec magna. Maecenas finibus efficitur ex. Nunc eget fermentum mi."
    },
    "sections": [
        {
            "order":1,
            "description":"Aşağıdaki çoktan seçmeli soruları yanıtlayın vs vs",
            "multipleChoices": [
                {
                    "num": 1,
                    "text": "ilk soru texti?",
                    "option1": "ilk secenek",
                    "option2": "22 secenek",
                    "option3": "3 secenek",
                    "option4": "4 secenek",
                    "correctAnswer": "ilk secenek"
                },
                {
                    "num": 2,
                    "text": "ikinci soru texti?",
                    "option1": "ilk secenek",
                    "option2": "22 secenek",
                    "option3": "3 secenek",
                    "option4": "4 secenek",
                    "option5": "5 secenek",
                    "correctAnswer": "3 secenek"
                }
            ]
        }, 
        {
            "order":2,
            "description":"Aşağıdaki sıralama sorularını yanıtlayın vs vs",
            "orderings": [
                {
                    "text": "Ornek cumle",
                    "correctOrder": 1
                },
                {
                    "text": "Ornek baska cumle",
                    "correctOrder": 2
                },
                {
                    "text": "Ornek bambaska cumle",
                    "correctOrder": 3
                }
            ]
        },
        {
            "order":3,
            "description":"Aşağıdaki T/F sorularını yanıtlayın vs vs",
            "trueFalses": [
                {
                    "text": "dogru cumle",
                    "correctAnswer": 1
                },
                {
                    "text": "yine dogru cumle",
                    "correctAnswer": 1
                },
                {
                    "text": "yanlis cumle",
                    "correctAnswer": 0
                },
                {
                    "text": "true cumle",
                    "correctAnswer": 1
                }
            ]
        },
        {
            "order":4,
            "description":"Aşağıdaki matching sorularını yanıtlayın vs vs",
            "matchings": [
                {
                    "number": 1,
                    "leftPart": "app",
                    "rightPart": "le"
                },
                {
                    "number": 2,
                    "leftPart": "tea",
                    "rightPart": "cher"
                },
                {
                    "number": 3,
                    "leftPart": "stu",
                    "rightPart": "dent"
                }
            ]
        },
        {
            "order":5,
            "description":"Aşağıdaki boşluk doldurma sorularını yanıtlayın vs vs",
            "gapFillingMain": {
                "clues": "table #*# apple #*# desk",
                "gapFillings": [
                    {
                        "num": 1,
                        "questionText": "the first statement #*# with a blank.",
                        "answer": "table"
                    },
                    {
                        "num": 2,
                        "questionText": "the second statement #*# with a blank.",
                        "answer": "apple"
                    },
                    {
                        "num": 3,
                        "questionText": "the third statement #*# with a blank.",
                        "answer": "desk"
                    }
                ]
            }
        }
    ]
}








```