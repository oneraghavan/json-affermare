Json-affermare
=========

Cucumber JVM add on library to verify JSON.

To add description

Usage
=========


Examples
-----

Empty object

                {}

                Then I verify that book is empty

Empty list

                []

                I verify that no authors are present

List of objects

                [
                    {
                            "id": 1000,
                            "name": "Kent Beck"
                    },
                    {
                            "id": 1001,
                            "name": "Martin Fowler"
                    }
                ]

                Then I verify that the following authors are present
                      | id      | name          |
                      | 1000    | Kent Beck     |
                      | 1001    | Martin Fowler |

                Then I verify that the number of authors are "2"

Values in object

                {
                        "id": 1000,
                        "name": "Kent Beck"
                }

                Then I verify that the following author is present
                      | id      | name      |
                      | 1000    | Kent Beck |

One to one association

                {
                        "isbn": "isbn123",
                        "name": "Test driven development"
                        "author":
                        {
                            "id": 1000,
                            "name": "Kent Beck"
                        }
                }

                Then I verify that book has a "author"
                  | id      | name          |
                  | 1000    | Kent Beck     |

One to many association

                {
                        "id": 1000,
                        "name": "Kent Beck"
                        "phone_numbers": [
                            {"type": "home", "number": 987654321},
                            {"type": "office", "number": 123456789}
                        ]
                }

                Then I verify that author has the following "phone_numbers"
                      | type        | number    |
                      | home        | 987654321 |
                      | office      | 123456789 |


Version
----

1.0

Tech
-----------

To be updated

Installation
--------------
Should be available in maven central soon.

License
----

MIT

Contribution
------------

Fork and send pull request

What's In the Name
------

All good english names are already taken by other json libraries - lets try italian.