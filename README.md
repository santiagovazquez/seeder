# seeder

## Usage
````js

const mySeeds = {
  carlos: {
    table: 'people',
    props: {
      name: 'Carlos' 
    },
    relations: {
      car_id: 'red_tesla.id'
    }
  },
  red_tesla: {
    table: 'cars',
    props: {
      model: 'S',
      brand: 'Tesla'
    }
  }
}

const { getModel, appendSeeds } = seedFn(mySeeds)


const carlosModel = getModel(mySeeds.carlos)

// prints id assined by db
console.log(carlosModel.id);


````
