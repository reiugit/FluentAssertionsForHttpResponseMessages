# FluentAssertionsForHttpResponseMessages

1.) Only with 'FluentAssertions'

        ok.StatusCode.Should().Be(HttpStatusCode.OK);  // 200
        ok.IsSuccessStatusCode.Should().BeTrue();      // 2xx

2.) Extended with 'HttpResponseMessageAssertions'

        ok.Should().HaveStatusCode(HttpStatusCode.OK);  // 200
        created.Should().BeSuccessful();                // 2xx
        badRequest.Should().HaveClientError();          // 4xx
        notFound.Should().HaveClientError();            // 4xx
        internalServerError.Should().HaveServerError(); // 5xx
