Write Code Exercises
---------------------
#.
    .. tabbed:: obj_writecode1

        .. tab:: Question

            .. activecode:: obj_writecode1q
                :nocodelens:

                Complete the following code to create an object ``spot`` from the ``Dog`` class
                with the name "Spot" and update their tricks to include "spin" then "sit". You can
                use ``print(spot)`` to print the string representation of the object.
                ~~~~
                class Dog:

                    def __init__(self, name):
                        self.name = name
                        self.tricks = []

                    def updateTricks(self, trick):
                        self.tricks.append(trick)

                    def __str__(self):
                        return 'Dog(name = ' + self.name +  ', tricks = ' + str(self.tricks) + ')'

                ====

                from unittest.gui import TestCaseGui

                class myTests(TestCaseGui):

                    def testOne(self):
                        self.assertEqual(spot.tricks, ['spin', 'sit'], 'Checking that sit and spin are added to the list of tricks.')
                        self.assertEqual(spot.__str__(), "Dog(name = Spot, tricks = ['spin', 'sit'])", 'Checking that a Spot prints correctly.')
                myTests().main()

        .. tab:: Answer

            .. activecode:: obj_writecode1a
                :optional:

                Below the class definition, create an instance of the class Dog, assigning it to the variable ``spot``.
                Be sure to include a name when constructing the instance! This works similar to a function.
                To update the dog's tricks, use the instance and dot notation to call the method, with the name of the trick as the argument.
                This needs to be done for each trick. Then, using the print function, you can print the dog's tricks and the contents of the ``__str__`` method.
                ~~~~
                class Dog:

                    def __init__(self, name):
                        self.name = name
                        self.tricks = []    # creates a new empty list for each dog

                    def updateTricks(self, trick):
                        self.tricks.append(trick)

                    def __str__(self):
                        return 'Dog(name = ' + self.name +  ', tricks = ' + str(self.tricks) + ')'

                spot = Dog('Spot')
                spot.updateTricks('spin')
                spot.updateTricks('sit')
                print(spot.tricks)
                print(spot)

#.
    .. activecode:: obj_writecode2

        Complete the following code to include a method named ``updateAttacks()``
        which updates the ``attacks`` list with the attacks of the pokemon.
        ~~~~
        class Pokemon:

            def __init__(self, name, kind):
                self.name = name
                self.type = kind
                self.attacks = []

            def __str__(self):
                return("Pokemon name is {} and type is {}. Attacks include: {}.".format(self.name, self.type, str(self.attacks)))

        bulbasaur = Pokemon('Bulbasaur', 'Grass')
        bulbasaur.updateAttacks('Vine Whip')
        bulbasaur.updateAttacks('Tackle')

        ====
        from unittest.gui import TestCaseGui

        class myTests(TestCaseGui):

            def testOne(self):
                pikachu = Pokemon('Pikachu','Electric')
                pikachu.updateAttacks('Quick Attack')
                self.assertEqual(pikachu.__str__(), "Pokemon name is Pikachu and type is Electric. Attacks include: ['Quick Attack'].", "Testing with Pikachu and Quick Attack")

        myTests().main()


#.
    .. tabbed:: obj_writecode3

        .. tab:: Question

          .. activecode:: obj_writecode3q
              :nocodelens:

              Correct the 7 errors in the following code. The program should create
              a class that prints the title and author of a book.
              ~~~~
              Class Book:

                  def __init__(title, author):
                      title = title
                      author = author
                  def __str__(self):
                      return("Your book is " + title + " by " + author)

              book = new Book("The Odyssey", "Homer")
              print(book)

              ====
              from unittest.gui import TestCaseGui

              class myTests(TestCaseGui):
                  def testOne(self):
                      gatsby = Book("The Great Gatsby", "F. Scott Fitzgerald")
                      self.assertEqual(gatsby.__str__(), "Your book is The Great Gatsby by F. Scott Fitzgerald", "Testing Great Gatsby")

              myTests().main()

        .. tab:: Answer

          .. activecode:: obj_writecode3a
              :optional:

              1. ``class`` is a reserved word and must be lowercase.
              2. class methods must include the self parameter as a reference to the current instance of the class. ``def __init__(self, title, author):``
              3. Use dot notation with the self instance to access the title variable in the Book class. ``self.title = title``
              4. Use dot notation with the self instance to access the author variable in the Book class. ``self.author = author``
              5. Use dot notation with the self instance to access the title variable when using it in a string. ``self.title``
              6. Use dot notation with the self instance to access the author variable when using it in a string. ``self.author``
              7. Use the correct class name, in this case it is ``Book`` not ``new Book``.

              ~~~~
              class Book:

                  def __init__(self, title, author):
                      self.title = title
                      self.author = author

                  def __str__(self):
                      return("Your book is " + self.title + " by " + self.author)

              book = Book("The Odyssey", "Homer")
              print(book)

#.
    .. activecode:: obj_writecode4
        :nocodelens:

        Correct the 7 errors in the following code. The program should create
        a class that prints the name and tricks of a dog.
        ~~~~
        class Dog

            def init(self, name):
                name = self.name
                self.tricks = []

            def updateTricks(self.trick):
                self.tricks.append = trick

            def __str__():
                return("The new dog is named { and his tricks are {}".format(self.name, str(self.tricks)))

        dog = new Dog('Toby')
        dog.updateTricks('catch')
        dog.updateTrick('spin')

        ====

        from unittest.gui import TestCaseGui

        class myTests(TestCaseGui):

            def testOne(self):
                self.assertEqual(dog.tricks, ['catch', 'sit'], 'Checking that catch and spin are added to the list of tricks.')
                self.assertEqual(dog.__str__(), "The new dog is named Toby and his tricks are ['catch', 'sit']", 'Checking that a Toby prints correctly.')
        myTests().main()

#.
    .. tabbed:: obj_writecode5

        .. tab:: Question

          .. activecode:: obj_writecode5q
              :nocodelens:

              Complete the following code to include a method named ``getTitle`` that returns
              the title and a method named ``getAuthor`` that returns the 'author'.
              ~~~~
              class Book:

                  def __init__(self, title, author):
                      self.title = title
                      self.author = author

              book = Book("The Odyssey", "Homer")
              print(book.getTitle())
              print(book.getAuthor())

              ====
              from unittest.gui import TestCaseGui

              class myTests(TestCaseGui):
                  def testOne(self):
                      gatsby = Book("The Great Gatsby", "F. Scott Fitzgerald")
                      self.assertEqual(gatsby.getAuthor(), "F. Scott Fitzgerald", "Testing Great Gatsby author")
                      self.assertEqual(gatsby.getTitle(), "The Great Gatsby", "Testing Great Gatsby title")


              myTests().main()



        .. tab:: Answer

          .. activecode:: obj_writecode5a
              :nocodelens:
              :optional:

              Create the ``getTitle`` and ``getAuthor`` methods just as you would define a function.
              Include the ``self`` parameter and use the self instance with dot notation to access
              title and author, as needed.
              ~~~~
              class Book:

                  def __init__(self, title, author):
                      self.title = title
                      self.author = author

                  # Create the methods using self to access the attributes
                  def getTitle(self):
                      return self.title

                  def getAuthor(self):
                      return self.author


              book = Book("The Odyssey", "Homer")
              print(book.getTitle())
              print(book.getAuthor())



#.
    .. activecode:: obj_writecode6

      Complete the following code to include a method named ``getTricks`` that returns the
      tricks list and a method named ``getName`` that returns the name when called.
      ~~~~
      class Dog:

          def __init__(self, name):
              self.name = name
              self.tricks = []

          def updateTricks(self, trick):
              self.tricks.append(trick)

      dog = Dog('Frito')
      dog.updateTricks('spin')
      dog.updateTricks('sit')
      print(dog.getName())
      print(dog.getTricks())


      ====
      from unittest.gui import TestCaseGui

      class myTests(TestCaseGui):
          def testOne(self):
              fido = Dog("Fido")
              fido.updateTricks("beg")
              self.assertEqual(fido.getName(), "Fido", "Testing a new dog with a new name")
              self.assertEqual(fido.getTricks(), ['beg'], "Testing that Fido has a new trick")


      myTests().main()

#.
    .. tabbed:: obj_writecode7

      .. tab:: Question

          .. activecode:: obj_writecode7q
              :nocodelens:

              Add a new class named ``Paperback`` that extends the ``Book`` class. Add a
              method named ``__str__`` within Paperback that sends a string representation
              for the Paperback book, reading ``"Paperback book [TITLE] was written by [AUTHOR]"``.
              ~~~~
              class Book:

                  def __init__(self, title, author):
                      self.title = title
                      self.author = author

                  def getTitle(self):
                      return self.title

                  def getAuthor(self):
                      return self.author

              book = Paperback("The Odyssey", "Homer")
              print(book)

              ====
              from unittest.gui import TestCaseGui

              class myTests(TestCaseGui):
                  def testOne(self):
                      gatsby = Paperback("The Great Gatsby", "F. Scott Fitzgerald")
                      self.assertEqual(gatsby.__str__(), "Paperback book The Great Gatsby was written by F. Scott Fitzgerald", "Testing Great Gatsby")

              myTests().main()


      .. tab:: Answer

          .. activecode:: obj_writecode7a
            :nocodelens:
            :optional:

            Create the ``Paperback`` class just as you did the ``Book`` class, but
            use the ``Book`` class as the parameter.
            Define the ``__str__`` function as usual, using instances from the parent class.
            ~~~~
            class Book:

                def __init__(self, title, author):
                    self.title = title
                    self.author = author

                def getTitle(self):
                    return self.title

                def getAuthor(self):
                    return self.author

            # Create Paperback class, using Book class
            class Paperback(Book):

                def __str__(self):
                    return ("Paperback book " + self.title + " was written by " + self.author)

            book = Paperback("The Odyssey", "Homer")
            print(book)

#.
    .. activecode:: obj_writecode8

      Update the new class named ``WaterType`` which inherits properties of the ``Pokemon`` class.
      Add the following three methods to WaterType: ``updateAttacks`` appends the attacks list with
      a new attack, ``getName`` returns the name, and ``getAttacks`` returns the attacks when called.
      ~~~~
      class Pokemon:

          def __init__(self, name):
              self.name = name
              self.attacks = []

      class WaterType(Pokemon):


      pokemon = WaterType('Gyrados')
      pokemon.updateAttacks('Twister')
      pokemon.updateAttacks('Whirlpool')
      print(pokemon.getName())
      print(pokemon.getAttacks())

      ====
      from unittest.gui import TestCaseGui

      class myTests(TestCaseGui):
          def testOne(self):
              horsea = WaterType("Horsea")
              horsea.updateAttacks("Water Gun")
              horsea.updateAttacks("Twister")
              self.assertEqual(horsea.getName(), "Horsea", "Testing a new Pokemon, Horsea")
              self.assertEqual(horsea.getAttacks(), ['Water Gun', 'Twister'], "Testing that Horsea has new tricks")

      myTests().main()

#.
    .. tabbed:: obj_writecode9

        .. tab:: Question

          .. activecode:: obj_writecode9q
              :nocodelens:

              Add a new class named ``Library`` that inherits the ``Book`` class.
              ``Library`` should have an initializer method that creates the list
              ``current_books``, where current books are stored, and a string method
              that returns the list. Also create a method called ``addBooks`` which
              adds a new book to ``current_books`` with both the title and author ``(title, author)``.
              ~~~~
              class Book:

                  def __init__(self, title, author):
                      self.title = title
                      self.author = author

                  def getTitle(self):
                      return self.title

                  def getAuthor(self):
                      return self.author

                  def __repr__(self):
                      return (self.title + " was written by " + self.author)

              ====
              from unittest.gui import TestCaseGui

              class myTests(TestCaseGui):
                  def testOne(self):
                      lib1 = Library()
                      lib1.add_book(Book("Pride and Prejudice", "Jane Austen"))
                      lib1.add_book(Book("The Great Gatsby","F. Scott Fitzgerald"))
                      self.assertEqual(lib1.__str__(), "[Pride and Prejudice was written by Jane Austen, The Great Gatsby was written by F. Scott Fitzgerald]", "Testing Pride and Prejudice and the Great Gatsby")
              myTests().main()

        .. tab:: Answer

          .. activecode:: obj_writecode9a
              :nocodelens:
              :optional:

              First, define the ``Library`` class so that it inherits ``Book``. Then
              use the initializer method to create the ``current_books`` list and the
              string method to return the list. Create a third method ``add_books`` to
              add new books to the list.
              ~~~~
              class Book:

                  def __init__(self, title, author):
                      self.title = title
                      self.author = author

                  def getTitle(self):
                      return self.title

                  def getAuthor(self):
                      return self.author

                  def __repr__(self):
                      return (self.title + " was written by " + self.author)

              class Library(Book):

                  def __init__(self):
                      self.current_books = []

                  def __str__(self):
                      return str(self.current_books)

                  def add_book(self, book):
                      self.current_books.append(book)

              lib1 = Library()
              lib1.add_book(Book("Pride and Prejudice", "Jane Austen"))
              print(lib1)

#.
    .. activecode:: obj_writecode10

      Add a new class named ``WaterType`` that inherits from Pokemon class. that takes 'name' as initial values, creates
      an instance of Pokemon with type as 'water' by default and stores the instance
      in a list named 'watertypes'. Also create a method called 'addPokemons' which
      takes 'name' as arguments, creates an instance of Pokemon and stores it in
      'watertypes'. Also create '__str__' that returns the string representation
      of the object that includes the 'watertypes' list.
      ~~~~
      class Pokemon:

          def __init__(self,name):
              self.name = name
              self.type = type

          def __repr__(self)
              return ( "Pokemon " self.name + " is of type" + self.type)

      newWater = WaterType("Magikarp")
      newWater.addPokemons("Krabby")
      print(newWater)
