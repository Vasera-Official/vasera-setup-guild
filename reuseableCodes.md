# Cards Section

<div className="flex items-center justify-between gap-4 md:flex-row flex-col">
    <Card className="flex-2">
        <CardHeader>
            <CardDescription>Total Notes</CardDescription>
        </CardHeader>
        <CardContent>
            <p className="text-4xl font-semibold">
                0
            </p>
        </CardContent>
        <CardFooter>
            <p className="text-sm text-muted-foreground">Notes created</p>
        </CardFooter>
    </Card>
</div>

# Big Banners

<div className="p-5 md:p-12 md:py-16 mt-6 bg-green-main rounded-lg shadow-md relative overflow-clip">
    <div>
        <h2 className="text-2xl md:text-5xl font-medium md:font-normal text-white">We are glad to <br /> have you on board</h2>
        <p className="text-white/50 md:text-white/90 pt-1 md:pt-6 pb-6">Lets get you up to speed, to make sure you get the best</p>

        <Button variant="secondary" onClick={()=>{navigate("/academic")}}>Setup Curriculum</Button>
    </div>
    <img src="/image/comp.png" alt="" className="hidden md:block w-[500px] absolute -bottom-8 right-0"/>

</div>

# No Content

<Card className="border-dashed border-2">
    <CardContent>
        <NoContent text="You haven't added any children yet. Click 'Add Child' to get started." />
    </CardContent>
</Card>
