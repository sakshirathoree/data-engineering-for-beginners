For example, in a typical e-commerce store, we might get data from payment systems like stripe, sales systems like Salesforce, marketing systems like Klaviyo.

Events coming in from the website, etc..

All these systems have their own APIs, which means we need to write code to connect to them and get their data into our storage, either periodically or depending on the use case, sometimes in real time.

### poc above one

Actually, some old systems grocery stores come to mind don't even have APIs, in which case they will

drop a large CSV on some shared storage system weekly or something like that.

Now, the storage system to store all this data from ingestion could be relational database like MySQL

or Postgres, or it could be an object storage system like AWS S3.

In practice, the storage part underpins the entire data pipeline because we must store the data throughout

the pipeline.

Okay, so once we ingest raw data, we transform this data in some way.

We've already talked about merging customer data and order data, but in reality this can be quite complex.

You might need to merge many different tables in a relational database, which may all come from different

sources and naming conventions.

In probably there are duplicate data, two or sometimes even conflicting data.

This has to be all cleaned up and combined to the kind of data our data consumers can make sense of.

And once we transform the data, we prepare it for serving it to our end customers for analytics, ML,

AI, or reverse ETL.

We'll delve into more details of these parts later.

Now here's a mental model that we find very helpful.

Compute versus storage.

What even is data?

It can seem abstract, but really it's just a piece of information.

But it's a piece of information that has to be changed from its original form to be useful.

So we change the data by using our computer's computing power or compute.

Once we use that compute to transform the data, we must store it because we'll need it more than once.

And that's storage.

I find it very helpful to clearly separate these two.

If you do, you'll understand the motivation behind a lot of the popular modern data engineering tools

we'll explore later.

You may have already noticed from the diagram here, but the top layer of the data pipeline involves

compute, and the bottom layer is made up of storage.

Now undercurrents cut through all stages of our data pipeline.

Some examples of undercurrents are orchestration, security, data governance, data ops, and data

quality.

These are critical concerns that every data engineering team should be aware of.

We'll cover each of these concepts in more detail in future lessons.


Play
